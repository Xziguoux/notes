#mlir 
[MLIR技术细节整理 - HarmonyHu’s Blog](https://harmonyhu.com/2021/08/17/mlir/)
[MLIR Language Reference - MLIR](https://mlir.llvm.org/docs/LangRef/)

## Operation

```bash
%2 = "toy.mul"(%0, %1) : (tensor<*xf64>, tensor<*xf64>) -> tensor<*xf64> loc("Toy/Ch2/codegen.toy":5:25)
```
- Operation 是通用定义，MulOp是特定定义
```cpp
mul_op = llvm::dyn_cast<MUlOp>()
op = mul_op.getOperation()
```
- 特定op可以直接访问属性，通用定义op无法访问特定属性，但可以间接访问
```cpp
// getAttrOfType
IntegerAttr opsetAttr = op->getAttrOfType<::mlir::Attribute>("onnx_opset").dyn_cast_or_null<IntegerAttr>();
if (opsetAttr)
  opset = opsetAttr.getValue().getSExtValue();
// getAttr
mlir::Type targetType = op->getAttr("to").cast<::mlir::TypeAttr>().getValue();
```

Operation常用api

```markmap
# mlir::Operation
## void erase()
## void remove()
## Block *getBlock()
## MLIRContext *getContext()
## Operation *getParentOp()
## template <typename OpTy> OpTy getParentOfType()
## void dump()
## unsigned getNumOperands()
## Value getOperand(unsigned idx)
## unsigned getNumResults()
## OpResult getResult(unsigned idx)
```

## mlir::Value
Value 可以理解成操作数，参数等


###  BlockArgument
```cpp
class BlockArgument : public Value{
  /// Returns the block that owns this argument.
  Block *getOwner() const { return getImpl()->owner; }

  /// Return the type of this value.
  Type getType() const { return getImpl()->type; }

  /// Set the type of this value.
  void setType(Type newType) { getImpl()->type = newType; }

  /// Returns the number of this argument.
  unsigned getArgNumber() const { return getImpl()->index; }
}
```
### OpResult

```cpp
class OpResult : public Value {
public:
  using Value::Value;

  static bool classof(Value value) {
    return value.getKind() != Kind::BlockArgument;
  }

  /// Returns the operation that owns this result.
  Operation *getOwner() const;

  /// Returns the number of this result.
  unsigned getResultNumber() const;
}

```
 通过value 获取 opeation
```cpp
// %2对应value，则
Operation * operation = value.getDefiningOp();
toy::MulOp op = value.getDefiningOp<toy::MulOp>();
// get Value from operation
Value inner_value = operation->getResult(0);
assert(inner_value == value);
```

## Type
type 可以理解成value的类型
常用接口有
```cpp
bool operator==(Type other) const { return impl == other.impl; }
bool operator!=(Type other) const { return !(*this == other); }
explicit operator bool() const { return impl; }
bool operator!() const { return impl == nullptr; }
template <typename U> bool isa() const;
template <typename First, typename Second, typename... Rest> bool isa() const;
template <typename U> U dyn_cast() const;
template <typename U> U dyn_cast_or_null() const;
template <typename U> U cast() const;
bool isIndex() const;
bool isBF16() const;
bool isF16() const;
bool isF32() const;
bool isF64() const;
bool isF80() const;
bool isF128() const;
/// Return true if this is an integer type with the specified width.
bool isInteger(unsigned width) const;
```

### ShapedType

### TensorType

## Attribute

```cpp
::mlir::Builder((*this)->getContext()).getF32FloatAttr(7.0)
::mlir::Builder((*this)->getContext()).getF64ArrayAttr({7., 8.})
::mlir::Builder((*this)->getContext()).getStrArrayAttr({"a", "b"})
```


## Block

block 在`{}`之间一系列 operation 的合集，一般 op 是没有 block，funcOp 会有一个 Block

## Region
一般情况下 op 是没有 region，在控制流 op 中会存在 region 的概念。一个 Region 包含 1 个或多个 Block，第一个 block 的 argument 也是 region 的 argument

## ModuleOp
最顶层op

## MLIRContext

用于创建全局的建造者 eg types，attributes

## OpBuilder
用于创建Operation

