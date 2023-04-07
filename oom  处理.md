- [x] 调节分配阈值大小 [[oom]] ✅ 2023-03-22
- [ ] 分op进行测试()
- [ ] 通过内存大小分析，进行分级过滤（正常/大内存）

```python
# rpc_cmd.append("sysctl -w vm.overcommit_ratio=80")
# rpc_cmd.append("echo -17 /proc/$(pgrep -f " + new_server_name +
# ")/oom_adj")
```