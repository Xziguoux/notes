---

annotation-target: file:///home/cambricon/data/note/optimizing_cp.pdf

---



>%%
>```annotation-json
>{"created":"2023-04-11T00:34:48.062Z","text":"全局变量的定义：\n- 函数之外申请的\n- 存储在静态内存区\n- static定义的静态变量也存储在静态区（包括浮点型常量，字符常量，数组初始化，switch声明跳表，虚函数表等）","updated":"2023-04-11T00:34:48.062Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":94043,"end":94122},{"type":"TextQuoteSelector","exact":"Variables that are declared outside of any function are called global variables","prefix":"turns. Global or static storage ","suffix":". They can be accessed from any "}]}]}
>```
>%%
>*%%PREFIX%%turns. Global or static storage%%HIGHLIGHT%% ==Variables that are declared outside of any function are called global variables== %%POSTFIX%%. They can be accessed from any*
>%%LINK%%[[#^vs8xgz2qr1|show annotation]]
>%%COMMENT%%
>全局变量的定义：
>- 函数之外申请的
>- 存储在静态内存区
>- static定义的静态变量也存储在静态区（包括浮点型常量，字符常量，数组初始化，switch声明跳表，虚函数表等）
>%%TAGS%%
>
^vs8xgz2qr1


>%%
>```annotation-json
>{"created":"2023-04-11T00:40:30.918Z","text":"静态数据区被分成三份：\n- 不背修改的程序变量\n- 可能被程序修改的初始化变量\n- 未被初始化的可能被修改的变量","updated":"2023-04-11T00:40:30.918Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":94436,"end":94493},{"type":"TextQuoteSelector","exact":"The static data area is usually divided into three parts:","prefix":", and virtual function tables.  ","suffix":" one for constants that are neve"}]}]}
>```
>%%
>*%%PREFIX%%, and virtual function tables.%%HIGHLIGHT%% ==The static data area is usually divided into three parts:== %%POSTFIX%%one for constants that are neve*
>%%LINK%%[[#^e1tgatg87t5|show annotation]]
>%%COMMENT%%
>静态数据区被分成三份：
>- 不背修改的程序变量
>- 可能被程序修改的初始化变量
>- 未被初始化的可能被修改的变量
>%%TAGS%%
>
^e1tgatg87t5


>%%
>```annotation-json
>{"created":"2023-04-11T00:44:36.024Z","updated":"2023-04-11T00:44:36.024Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":94693,"end":94889},{"type":"TextQuoteSelector","exact":"The advantage of static data is that it can be initialized to desired values before the program starts. The disadvantage is that the memory space is occupied throughout the whole program execution","prefix":"ay be modified by the program.  ","suffix":", even if the variable is only u"}]}]}
>```
>%%
>*%%PREFIX%%ay be modified by the program.%%HIGHLIGHT%% ==The advantage of static data is that it can be initialized to desired values before the program starts. The disadvantage is that the memory space is occupied throughout the whole program execution== %%POSTFIX%%, even if the variable is only u*
>%%LINK%%[[#^td63sp9q1gn|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^td63sp9q1gn


>%%
>```annotation-json
>{"created":"2023-04-11T00:45:59.498Z","updated":"2023-04-11T00:45:59.498Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":95060,"end":95109},{"type":"TextQuoteSelector","exact":"Do not make variables global if you can avoid it.","prefix":"be reused for another purpose.  ","suffix":" Global variables may be needed "}]}]}
>```
>%%
>*%%PREFIX%%be reused for another purpose.%%HIGHLIGHT%% ==Do not make variables global if you can avoid it.== %%POSTFIX%%Global variables may be needed*
>%%LINK%%[[#^zhq0mrudl2|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^zhq0mrudl2


>%%
>```annotation-json
>{"created":"2023-04-11T00:47:53.783Z","updated":"2023-04-11T00:47:53.783Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":95429,"end":95648},{"type":"TextQuoteSelector","exact":" But it may be a better solution to make the functions that access the saved variable members of the same class and store the shared variable inside the class. Which solution you prefer is a matter of programming style.","prefix":" variable as function parameter.","suffix":"  It is preferable to declare a "}]}]}
>```
>%%
>*%%PREFIX%%variable as function parameter.%%HIGHLIGHT%% ==But it may be a better solution to make the functions that access the saved variable members of the same class and store the shared variable inside the class. Which solution you prefer is a matter of programming style.== %%POSTFIX%%It is preferable to declare a*
>%%LINK%%[[#^t55td7mrrzb|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^t55td7mrrzb


>%%
>```annotation-json
>{"created":"2023-04-11T00:49:07.353Z","updated":"2023-04-11T00:49:07.353Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":95849,"end":95953},{"type":"TextQuoteSelector","exact":"The advantage of this is that the list does not need to be initialized every time the function is called","prefix":".4, 2.5};    return list[x]; }  ","suffix":". The static declaration helps t"}]}]}
>```
>%%
>*%%PREFIX%%.4, 2.5};    return list[x]; }%%HIGHLIGHT%% ==The advantage of this is that the list does not need to be initialized every time the function is called== %%POSTFIX%%. The static declaration helps t*
>%%LINK%%[[#^8wupt5lbna8|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^8wupt5lbna8



>%%
>```annotation-json
>{"created":"2023-04-11T00:51:49.061Z","updated":"2023-04-11T00:51:49.061Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":96060,"end":96082},{"type":"TextQuoteSelector","exact":"The const declaration ","prefix":"used from one call to the next. ","suffix":"helps the compiler see that the "}]}]}
>```
>%%
>*%%PREFIX%%used from one call to the next.%%HIGHLIGHT%% ==The const declaration== %%POSTFIX%%helps the compiler see that the*
>%%LINK%%[[#^gexhz1t8phn|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^gexhz1t8phn


>%%
>```annotation-json
>{"created":"2023-04-11T00:55:12.999Z","updated":"2023-04-11T00:55:12.999Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":96315,"end":96452},{"type":"TextQuoteSelector","exact":"This is inefficient because the function needs extra overhead to check whether it called for the first time or it has been called before.","prefix":"d, but not on subsequent calls. ","suffix":" The const declaration helps the"}]}]}
>```
>%%
>*%%PREFIX%%d, but not on subsequent calls.%%HIGHLIGHT%% ==This is inefficient because the function needs extra overhead to check whether it called for the first time or it has been called before.== %%POSTFIX%%The const declaration helps the*
>%%LINK%%[[#^jn6nd4cgcyj|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^jn6nd4cgcyj


>%%
>```annotation-json
>{"created":"2023-04-11T00:55:55.103Z","updated":"2023-04-11T00:55:55.103Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":95955,"end":95977},{"type":"TextQuoteSelector","exact":"The static declaration","prefix":"ry time the function is called. ","suffix":" helps the compiler decide that "}]}]}
>```
>%%
>*%%PREFIX%%ry time the function is called.%%HIGHLIGHT%% ==The static declaration== %%POSTFIX%%helps the compiler decide that*
>%%LINK%%[[#^g5qy9p4rnbp|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^g5qy9p4rnbp


>%%
>```annotation-json
>{"created":"2023-04-11T00:57:06.472Z","updated":"2023-04-11T00:57:06.472Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":97026,"end":97163},{"type":"TextQuoteSelector","exact":"All identical constants in the entire program will be joined together in order to minimize the amount of cache space used for constants. ","prefix":"ne constant needs to be stored. ","suffix":" Integer constants are usually i"}]}]}
>```
>%%
>*%%PREFIX%%ne constant needs to be stored.%%HIGHLIGHT%% ==All identical constants in the entire program will be joined together in order to minimize the amount of cache space used for constants.== %%POSTFIX%%Integer constants are usually i*
>%%LINK%%[[#^3d4kuan3n5g|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^3d4kuan3n5g



>%%
>```annotation-json
>{"created":"2023-04-11T00:59:37.890Z","updated":"2023-04-11T00:59:37.890Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":97164,"end":97308},{"type":"TextQuoteSelector","exact":"Integer constants are usually included as part of the instruction code. You can assume that there are no caching problems for integer constants.","prefix":"ache space used for constants.  ","suffix":" Register storage A limited numb"}]}]}
>```
>%%
>*%%PREFIX%%ache space used for constants.%%HIGHLIGHT%% ==Integer constants are usually included as part of the instruction code. You can assume that there are no caching problems for integer constants.== %%POSTFIX%%Register storage A limited numb*
>%%LINK%%[[#^5x6yjk5fwl8|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^5x6yjk5fwl8


>%%
>```annotation-json
>{"created":"2023-04-11T01:03:12.138Z","updated":"2023-04-11T01:03:12.138Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":97774,"end":97890},{"type":"TextQuoteSelector","exact":"Local variables are particularly suited for register storage. This is another reason for preferring local variables.","prefix":" (live ranges) do not overlap.  ","suffix":"   The number of registers is li"}]}]}
>```
>%%
>*%%PREFIX%%(live ranges) do not overlap.%%HIGHLIGHT%% ==Local variables are particularly suited for register storage. This is another reason for preferring local variables.== %%POSTFIX%%The number of registers is li*
>%%LINK%%[[#^zet6k47kxf9|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^zet6k47kxf9


>%%
>```annotation-json
>{"created":"2023-04-11T01:03:31.243Z","updated":"2023-04-11T01:03:31.243Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":97893,"end":98088},{"type":"TextQuoteSelector","exact":"The number of registers is limited. There are approximately six integer registers available for general purposes in 32-bit x86 operating systems and fourteen integer registers in 64-bit systems. ","prefix":"r preferring local variables.   ","suffix":" Floating point variables use a "}]}]}
>```
>%%
>*%%PREFIX%%r preferring local variables.%%HIGHLIGHT%% ==The number of registers is limited. There are approximately six integer registers available for general purposes in 32-bit x86 operating systems and fourteen integer registers in 64-bit systems.== %%POSTFIX%%Floating point variables use a*
>%%LINK%%[[#^3cgw0dky7af|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^3cgw0dky7af


>%%
>```annotation-json
>{"created":"2023-04-11T01:04:01.867Z","updated":"2023-04-11T01:04:01.867Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":98089,"end":98484},{"type":"TextQuoteSelector","exact":"Floating point variables use a different kind of registers. There are eight floating point registers available in 32-bit operating systems, sixteen in 64-bit operating systems, and thirty two when the AVX512 instruction set is enabled in 64-bit mode. Some compilers have difficulties making floating point register variables in 32-bit mode unless the SSE instruction set (or higher) is enabled. ","prefix":"r registers in 64-bit systems.  ","suffix":"Volatile The volatile keyword sp"}]}]}
>```
>%%
>*%%PREFIX%%r registers in 64-bit systems.%%HIGHLIGHT%% ==Floating point variables use a different kind of registers. There are eight floating point registers available in 32-bit operating systems, sixteen in 64-bit operating systems, and thirty two when the AVX512 instruction set is enabled in 64-bit mode. Some compilers have difficulties making floating point register variables in 32-bit mode unless the SSE instruction set (or higher) is enabled.== %%POSTFIX%%Volatile The volatile keyword sp*
>%%LINK%%[[#^cv1kzk7w83l|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^cv1kzk7w83l


>%%
>```annotation-json
>{"created":"2023-04-11T01:06:17.207Z","updated":"2023-04-11T01:06:17.207Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":99165,"end":99186},{"type":"TextQuoteSelector","exact":" seconds remains zero","prefix":"izing compiler would assume that","suffix":" in the while loop because nothi"}]}]}
>```
>%%
>*%%PREFIX%%izing compiler would assume that%%HIGHLIGHT%% ==seconds remains zero== %%POSTFIX%%in the while loop because nothi*
>%%LINK%%[[#^skjnylqg3pf|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^skjnylqg3pf


>%%
>```annotation-json
>{"created":"2023-04-11T01:06:56.078Z","updated":"2023-04-11T01:06:56.078Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":99328,"end":99490},{"type":"TextQuoteSelector","exact":"The effect of the keyword volatile is that it makes sure the variable is stored in memory rather than in a register and prevents all optimizations on the variable","prefix":"ich would be an infinite loop.  ","suffix":". This can be useful in test sit"}]}]}
>```
>%%
>*%%PREFIX%%ich would be an infinite loop.%%HIGHLIGHT%% ==The effect of the keyword volatile is that it makes sure the variable is stored in memory rather than in a register and prevents all optimizations on the variable== %%POSTFIX%%. This can be useful in test sit*
>%%LINK%%[[#^u5a6udqncy|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^u5a6udqncy


>%%
>```annotation-json
>{"created":"2023-04-11T01:07:20.010Z","updated":"2023-04-11T01:07:20.010Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":99580,"end":99620},{"type":"TextQuoteSelector","exact":"Note that volatile does not mean atomic.","prefix":" expression is optimized away.  ","suffix":" It will not prevent two threads"}]}]}
>```
>%%
>*%%PREFIX%%expression is optimized away.%%HIGHLIGHT%% ==Note that volatile does not mean atomic.== %%POSTFIX%%It will not prevent two threads*
>%%LINK%%[[#^syzb4b6fut|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^syzb4b6fut


>%%
>```annotation-json
>{"created":"2023-04-11T01:08:24.699Z","updated":"2023-04-11T01:08:24.699Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":100185,"end":100298},{"type":"TextQuoteSelector","exact":"Thread-local storage is inefficient because it is accessed through a pointer stored in a thread environment block","prefix":"e one instance for each thread. ","suffix":". Static thread-local storage sh"}]}]}
>```
>%%
>*%%PREFIX%%e one instance for each thread.%%HIGHLIGHT%% ==Thread-local storage is inefficient because it is accessed through a pointer stored in a thread environment block== %%POSTFIX%%. Static thread-local storage sh*
>%%LINK%%[[#^0roozwh217wh|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^0roozwh217wh


>%%
>```annotation-json
>{"created":"2023-04-11T01:08:50.409Z","updated":"2023-04-11T01:08:50.409Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":100300,"end":100410},{"type":"TextQuoteSelector","exact":"Static thread-local storage should be avoided, if possible, and replaced by storage on the thread's own stack ","prefix":" in a thread environment block. ","suffix":"(see above, p. 25). Non-static v"}]}]}
>```
>%%
>*%%PREFIX%%in a thread environment block.%%HIGHLIGHT%% ==Static thread-local storage should be avoided, if possible, and replaced by storage on the thread's own stack== %%POSTFIX%%(see above, p. 25). Non-static v*
>%%LINK%%[[#^agzx9bm6rwh|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^agzx9bm6rwh


>%%
>```annotation-json
>{"created":"2023-04-11T01:10:51.872Z","updated":"2023-04-11T01:10:51.872Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":100593,"end":100803},{"type":"TextQuoteSelector","exact":"These variables and objects will have a separate instance for each thread. The need for static thread-local storage can be avoided in most cases by declaring the variables or objects inside the thread function.","prefix":"e stored on the thread's stack. ","suffix":" Far Systems with segmented memo"}]}]}
>```
>%%
>*%%PREFIX%%e stored on the thread's stack.%%HIGHLIGHT%% ==These variables and objects will have a separate instance for each thread. The need for static thread-local storage can be avoided in most cases by declaring the variables or objects inside the thread function.== %%POSTFIX%%Far Systems with segmented memo*
>%%LINK%%[[#^9wrlawq17f7|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^9wrlawq17f7


>%%
>```annotation-json
>{"created":"2023-04-11T01:13:10.224Z","updated":"2023-04-11T01:13:10.224Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":101751,"end":101926},{"type":"TextQuoteSelector","exact":"Objects that are allocated in sequence are not necessarily stored sequentially in memory. They may be scattered around at different places when the heap has become fragmented.","prefix":"s is called garbage collection. ","suffix":" This makes data caching ineffic"}]}]}
>```
>%%
>*%%PREFIX%%s is called garbage collection.%%HIGHLIGHT%% ==Objects that are allocated in sequence are not necessarily stored sequentially in memory. They may be scattered around at different places when the heap has become fragmented.== %%POSTFIX%%This makes data caching ineffic*
>%%LINK%%[[#^t34zs8vlm9q|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^t34zs8vlm9q


>%%
>```annotation-json
>{"created":"2023-04-11T01:16:10.455Z","updated":"2023-04-11T01:16:10.455Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":102478,"end":102582},{"type":"TextQuoteSelector","exact":"See page 95 for a further discussion of the advantages and drawbacks of using dynamic memory allocation.","prefix":"erhead to prevent such errors.  ","suffix":"  Some programming languages, su"}]}]}
>```
>%%
>*%%PREFIX%%erhead to prevent such errors.%%HIGHLIGHT%% ==See page 95 for a further discussion of the advantages and drawbacks of using dynamic memory allocation.== %%POSTFIX%%Some programming languages, su*
>%%LINK%%[[#^12u0vjydl17b|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^12u0vjydl17b


>%%
>```annotation-json
>{"created":"2023-04-11T01:16:49.091Z","updated":"2023-04-11T01:16:49.091Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":102738,"end":102841},{"type":"TextQuoteSelector","exact":"Variables declared inside a class are stored in the order in which they appear in the class declaration","prefix":"riables declared inside a class ","suffix":". The type of storage is determi"}]}]}
>```
>%%
>*%%PREFIX%%riables declared inside a class%%HIGHLIGHT%% ==Variables declared inside a class are stored in the order in which they appear in the class declaration== %%POSTFIX%%. The type of storage is determi*
>%%LINK%%[[#^0ybhizlcqtac|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^0ybhizlcqtac


>%%
>```annotation-json
>{"created":"2023-04-11T01:20:20.588Z","updated":"2023-04-11T01:20:20.588Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":103136,"end":103256},{"type":"TextQuoteSelector","exact":"A class member variable with the static modifier will be stored in static memory and will have one and only one instance","prefix":" can be copied into registers.  ","suffix":". Non-static members of the same"}]}]}
>```
>%%
>*%%PREFIX%%can be copied into registers.%%HIGHLIGHT%% ==A class member variable with the static modifier will be stored in static memory and will have one and only one instance== %%POSTFIX%%. Non-static members of the same*
>%%LINK%%[[#^h6equcs6ym|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^h6equcs6ym


>%%
>```annotation-json
>{"created":"2023-04-11T01:26:40.213Z","updated":"2023-04-11T01:26:40.213Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":103348,"end":103565},{"type":"TextQuoteSelector","exact":"Storing variables in a class or structure is a good way of making sure that variables that are used in the same part of the program are also stored near each other. See page 52 for the pros and cons of using classes. ","prefix":"ach instance of the class.  29  ","suffix":" 7.2 Integers variables and oper"}]}]}
>```
>%%
>*%%PREFIX%%ach instance of the class.  29%%HIGHLIGHT%% ==Storing variables in a class or structure is a good way of making sure that variables that are used in the same part of the program are also stored near each other. See page 52 for the pros and cons of using classes.== %%POSTFIX%%7.2 Integers variables and oper*
>%%LINK%%[[#^fjfpcw7km54|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^fjfpcw7km54


>%%
>```annotation-json
>{"created":"2023-04-11T01:29:50.984Z","updated":"2023-04-11T01:29:50.984Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":104639,"end":104705},{"type":"TextQuoteSelector","exact":"Integer operations are fast in most cases, regardless of the size.","prefix":"eger types of a specific size.  ","suffix":" However, it is inefficient to u"}]}]}
>```
>%%
>*%%PREFIX%%eger types of a specific size.%%HIGHLIGHT%% ==Integer operations are fast in most cases, regardless of the size.== %%POSTFIX%%However, it is inefficient to u*
>%%LINK%%[[#^ppgqaz8v6pf|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^ppgqaz8v6pf


>%%
>```annotation-json
>{"created":"2023-04-11T01:30:42.319Z","updated":"2023-04-11T01:30:42.319Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":104706,"end":104811},{"type":"TextQuoteSelector","exact":"However, it is inefficient to use an integer size that is larger than the largest available register size","prefix":" cases, regardless of the size. ","suffix":". In other words, it is ineffici"}]}]}
>```
>%%
>*%%PREFIX%%cases, regardless of the size.%%HIGHLIGHT%% ==However, it is inefficient to use an integer size that is larger than the largest available register size== %%POSTFIX%%. In other words, it is ineffici*
>%%LINK%%[[#^mpw085x6cg|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^mpw085x6cg


>%%
>```annotation-json
>{"created":"2023-04-11T01:31:58.116Z","updated":"2023-04-11T01:31:58.116Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":105181,"end":105346},{"type":"TextQuoteSelector","exact":"In many cases, the compiler will convert these types to integers of the default size when doing calculations, and then use only the lower 8 or 16 bits of the result.","prefix":"e only slightly less efficient. ","suffix":" You can assume that the type co"}]}]}
>```
>%%
>*%%PREFIX%%e only slightly less efficient.%%HIGHLIGHT%% ==In many cases, the compiler will convert these types to integers of the default size when doing calculations, and then use only the lower 8 or 16 bits of the result.== %%POSTFIX%%You can assume that the type co*
>%%LINK%%[[#^4llahrgpzna|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^4llahrgpzna


>%%
>```annotation-json
>{"created":"2023-04-11T01:37:43.123Z","updated":"2023-04-11T01:37:43.123Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":105347,"end":105416},{"type":"TextQuoteSelector","exact":"You can assume that the type conversion takes zero or one clock cycle","prefix":"wer 8 or 16 bits of the result. ","suffix":". In 64-bit systems, there is on"}]}]}
>```
>%%
>*%%PREFIX%%wer 8 or 16 bits of the result.%%HIGHLIGHT%% ==You can assume that the type conversion takes zero or one clock cycle== %%POSTFIX%%. In 64-bit systems, there is on*
>%%LINK%%[[#^lxwonj5fs3|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^lxwonj5fs3


>%%
>```annotation-json
>{"created":"2023-04-11T01:48:37.666Z","updated":"2023-04-11T01:48:37.666Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":105576,"end":105724},{"type":"TextQuoteSelector","exact":"It is recommended to use the default integer size in cases where the size does not matter and there is no risk of overflow, such as simple variables","prefix":"s you are not doing divisions.  ","suffix":", loop counters, etc. In large a"}]}]}
>```
>%%
>*%%PREFIX%%s you are not doing divisions.%%HIGHLIGHT%% ==It is recommended to use the default integer size in cases where the size does not matter and there is no risk of overflow, such as simple variables== %%POSTFIX%%, loop counters, etc. In large a*
>%%LINK%%[[#^6160ygjxpvn|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^6160ygjxpvn


>%%
>```annotation-json
>{"created":"2023-04-12T00:35:37.888Z","updated":"2023-04-12T00:35:37.888Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":105746,"end":105905},{"type":"TextQuoteSelector","exact":"In large arrays, it may be preferred to use the smallest integer size that is big enough for the specific purpose in order to make better use of the data cache","prefix":" variables, loop counters, etc. ","suffix":". Bit-fields of sizes other than"}]}]}
>```
>%%
>*%%PREFIX%%variables, loop counters, etc.%%HIGHLIGHT%% ==In large arrays, it may be preferred to use the smallest integer size that is big enough for the specific purpose in order to make better use of the data cache== %%POSTFIX%%. Bit-fields of sizes other than*
>%%LINK%%[[#^iseyq4i0ny8|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^iseyq4i0ny8


>%%
>```annotation-json
>{"created":"2023-04-12T00:37:28.207Z","updated":"2023-04-12T00:37:28.207Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":106083,"end":106174},{"type":"TextQuoteSelector","exact":"The unsigned integer type size_t is 32 bits in 32-bit systems and 64 bits in 64-bit systems","prefix":"an make use of the extra bits.  ","suffix":". It is intended for array sizes"}]}]}
>```
>%%
>*%%PREFIX%%an make use of the extra bits.%%HIGHLIGHT%% ==The unsigned integer type size_t is 32 bits in 32-bit systems and 64 bits in 64-bit systems== %%POSTFIX%%. It is intended for array sizes*
>%%LINK%%[[#^h8h9ith4n3w|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^h8h9ith4n3w


>%%
>```annotation-json
>{"created":"2023-04-12T00:38:01.605Z","updated":"2023-04-12T00:38:01.605Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":106422,"end":106469},{"type":"TextQuoteSelector","exact":"if intermediate calculations can cause overflow","prefix":"ific purpose, you must consider ","suffix":". For example, in the expression"}]}]}
>```
>%%
>*%%PREFIX%%ific purpose, you must consider%%HIGHLIGHT%% ==if intermediate calculations can cause overflow== %%POSTFIX%%. For example, in the expression*
>%%LINK%%[[#^22xjbgr1j6x|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^22xjbgr1j6x


>%%
>```annotation-json
>{"created":"2023-04-12T00:38:13.449Z","updated":"2023-04-12T00:38:13.449Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":106491,"end":106609},{"type":"TextQuoteSelector","exact":"expression a = (b*c)/d, it can happen that (b*c) overflows, even if a, b, c and d would all be below the maximum value","prefix":"e overflow. For example, in the ","suffix":". There is no automatic check fo"}]}]}
>```
>%%
>*%%PREFIX%%e overflow. For example, in the%%HIGHLIGHT%% ==expression a = (b*c)/d, it can happen that (b*c) overflows, even if a, b, c and d would all be below the maximum value== %%POSTFIX%%. There is no automatic check fo*
>%%LINK%%[[#^zqizv1fqqgf|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^zqizv1fqqgf


>%%
>```annotation-json
>{"created":"2023-04-12T00:39:39.892Z","updated":"2023-04-12T00:39:39.892Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":106694,"end":106828},{"type":"TextQuoteSelector","exact":"In most cases, there is no difference in speed between using signed and unsigned integers. But there are a few cases where it matters:","prefix":"Signed versus unsigned integers ","suffix":"  • Division by a constant: Unsi"}]}]}
>```
>%%
>*%%PREFIX%%Signed versus unsigned integers%%HIGHLIGHT%% ==In most cases, there is no difference in speed between using signed and unsigned integers. But there are a few cases where it matters:== %%POSTFIX%%• Division by a constant: Unsi*
>%%LINK%%[[#^s1w0864oju|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^s1w0864oju


>%%
>```annotation-json
>{"created":"2023-04-12T00:39:51.516Z","updated":"2023-04-12T00:39:51.516Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":106832,"end":106854},{"type":"TextQuoteSelector","exact":"Division by a constant","prefix":" few cases where it matters:  • ","suffix":": Unsigned is faster than signed"}]}]}
>```
>%%
>*%%PREFIX%%few cases where it matters:  •%%HIGHLIGHT%% ==Division by a constant== %%POSTFIX%%: Unsigned is faster than signed*
>%%LINK%%[[#^ef5vr0yon5v|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^ef5vr0yon5v


>%%
>```annotation-json
>{"created":"2023-04-12T00:40:17.318Z","updated":"2023-04-12T00:40:17.318Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":106995,"end":107101},{"type":"TextQuoteSelector","exact":"Conversion to floating point is faster with signed than with unsigned integers for most instruction sets. ","prefix":" to the modulo operator %.    • ","suffix":" • Overflow behaves differently "}]}]}
>```
>%%
>*%%PREFIX%%to the modulo operator %.    •%%HIGHLIGHT%% ==Conversion to floating point is faster with signed than with unsigned integers for most instruction sets.== %%POSTFIX%%• Overflow behaves differently*
>%%LINK%%[[#^82gf34z8pca|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^82gf34z8pca


>%%
>```annotation-json
>{"created":"2023-04-12T00:41:26.670Z","updated":"2023-04-12T00:41:26.670Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":107167,"end":107292},{"type":"TextQuoteSelector","exact":"An overflow of an unsigned variable produces a low positive result. An overflow of a signed variable is officially undefined.","prefix":" signed and unsigned variables. ","suffix":" The normal behavior is wrap-aro"}]}]}
>```
>%%
>*%%PREFIX%%signed and unsigned variables.%%HIGHLIGHT%% ==An overflow of an unsigned variable produces a low positive result. An overflow of a signed variable is officially undefined.== %%POSTFIX%%The normal behavior is wrap-aro*
>%%LINK%%[[#^fiyypb0xdr|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^fiyypb0xdr


>%%
>```annotation-json
>{"created":"2023-04-12T00:44:52.362Z","updated":"2023-04-12T00:44:52.362Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":108029,"end":108092},{"type":"TextQuoteSelector","exact":"this works only if it is certain that a will never be negative.","prefix":"the division faster. Of course, ","suffix":" The last line is implicitly con"}]}]}
>```
>%%
>*%%PREFIX%%the division faster. Of course,%%HIGHLIGHT%% ==this works only if it is certain that a will never be negative.== %%POSTFIX%%The last line is implicitly con*
>%%LINK%%[[#^u3b97lj1y0i|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^u3b97lj1y0i


>%%
>```annotation-json
>{"created":"2023-04-12T00:45:43.591Z","updated":"2023-04-12T00:45:43.591Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":108631,"end":108675},{"type":"TextQuoteSelector","exact":"Multiplication and division take longer time","prefix":"cycle on most microprocessors.  ","suffix":". Integer multiplication takes 1"}]}]}
>```
>%%
>*%%PREFIX%%cycle on most microprocessors.%%HIGHLIGHT%% ==Multiplication and division take longer time== %%POSTFIX%%. Integer multiplication takes 1*
>%%LINK%%[[#^kkf8bvvfj7g|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^kkf8bvvfj7g


>%%
>```annotation-json
>{"created":"2023-04-12T00:46:31.374Z","updated":"2023-04-12T00:46:31.374Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":109466,"end":109520},{"type":"TextQuoteSelector","exact":"for (i=0; i<n; i++) is the same as for (i=0; i<n; ++i)","prefix":" simply identical. For example, ","suffix":". But when the result of the exp"}]}]}
>```
>%%
>*%%PREFIX%%simply identical. For example,%%HIGHLIGHT%% ==for (i=0; i<n; i++) is the same as for (i=0; i<n; ++i)== %%POSTFIX%%. But when the result of the exp*
>%%LINK%%[[#^com59qisorh|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^com59qisorh


>%%
>```annotation-json
>{"created":"2023-04-12T00:49:40.162Z","updated":"2023-04-12T00:49:40.162Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":109628,"end":109870},{"type":"TextQuoteSelector","exact":"x = array[i++] is more efficient than x = array[++i] because in the latter case, the calculation of the address of the array element has to wait for the new value of i which will delay the availability of x for approximately two clock cycles.","prefix":"nce in efficiency. For example, ","suffix":" Obviously, the initial value of"}]}]}
>```
>%%
>*%%PREFIX%%nce in efficiency. For example,%%HIGHLIGHT%% ==x = array[i++] is more efficient than x = array[++i] because in the latter case, the calculation of the address of the array element has to wait for the new value of i which will delay the availability of x for approximately two clock cycles.== %%POSTFIX%%Obviously, the initial value of*
>%%LINK%%[[#^419o3xuy8p2|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^419o3xuy8p2


>%%
>```annotation-json
>{"created":"2023-04-12T00:51:05.440Z","updated":"2023-04-12T00:51:05.440Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":110709,"end":110909},{"type":"TextQuoteSelector","exact":"The original method of doing floating point operations involves eight floating point registers organized as a register stack, called x87 registers. These registers have long double precision (80 bits)","prefix":" advantages and disadvantages.  ","suffix":". The advantages of using the re"}]}]}
>```
>%%
>*%%PREFIX%%advantages and disadvantages.%%HIGHLIGHT%% ==The original method of doing floating point operations involves eight floating point registers organized as a register stack, called x87 registers. These registers have long double precision (80 bits)== %%POSTFIX%%. The advantages of using the re*
>%%LINK%%[[#^r7wc90yf9nq|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^r7wc90yf9nq


>%%
>```annotation-json
>{"created":"2023-04-12T00:52:34.310Z","updated":"2023-04-12T00:52:34.310Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":111651,"end":111785},{"type":"TextQuoteSelector","exact":"A newer method of doing floating point operations involves vector registers (XMM, YMM, or ZMM) which can be used for multiple purposes","prefix":" double precision is used.   32 ","suffix":". Floating point operations are "}]}]}
>```
>%%
>*%%PREFIX%%double precision is used.   32%%HIGHLIGHT%% ==A newer method of doing floating point operations involves vector registers (XMM, YMM, or ZMM) which can be used for multiple purposes== %%POSTFIX%%. Floating point operations are*
>%%LINK%%[[#^mscwn2djplc|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^mscwn2djplc


>%%
>```annotation-json
>{"created":"2023-04-12T00:55:35.948Z","updated":"2023-04-12T00:55:35.948Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":112177,"end":112194},{"type":"TextQuoteSelector","exact":"Disadvantages are","prefix":"tor registers (see page 115).   ","suffix":":  • Long double precision is no"}]}]}
>```
>%%
>*%%PREFIX%%tor registers (see page 115).%%HIGHLIGHT%% ==Disadvantages are== %%POSTFIX%%:  • Long double precision is no*
>%%LINK%%[[#^947lzen821q|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^947lzen821q


>%%
>```annotation-json
>{"created":"2023-04-12T00:55:43.708Z","updated":"2023-04-12T00:55:43.708Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":111943,"end":111992},{"type":"TextQuoteSelector","exact":"The advantages of using the vector registers are:","prefix":"same precision as the operands. ","suffix":"  • It is easy to make floating "}]}]}
>```
>%%
>*%%PREFIX%%same precision as the operands.%%HIGHLIGHT%% ==The advantages of using the vector registers are:== %%POSTFIX%%• It is easy to make floating*
>%%LINK%%[[#^ut023r7p1nq|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^ut023r7p1nq


>%%
>```annotation-json
>{"created":"2023-04-12T01:01:45.569Z","updated":"2023-04-12T01:01:45.569Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":113152,"end":113280},{"type":"TextQuoteSelector","exact":"In most cases, double precision calculations take no more time than single precision as long as they are not joined into vectors","prefix":" optimal for each calculation.  ","suffix":". Single precision division, squ"}]}]}
>```
>%%
>*%%PREFIX%%optimal for each calculation.%%HIGHLIGHT%% ==In most cases, double precision calculations take no more time than single precision as long as they are not joined into vectors== %%POSTFIX%%. Single precision division, squ*
>%%LINK%%[[#^g3fvd8l3ng7|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^g3fvd8l3ng7


>%%
>```annotation-json
>{"created":"2023-04-12T01:02:28.489Z","updated":"2023-04-12T01:02:28.489Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":113588,"end":113693},{"type":"TextQuoteSelector","exact":"You may use double precision without worrying too much about the costs if it is good for the application.","prefix":"ector operations are not used.  ","suffix":" You may use single precision if"}]}]}
>```
>%%
>*%%PREFIX%%ector operations are not used.%%HIGHLIGHT%% ==You may use double precision without worrying too much about the costs if it is good for the application.== %%POSTFIX%%You may use single precision if*
>%%LINK%%[[#^gq6fe9d4svt|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^gq6fe9d4svt


>%%
>```annotation-json
>{"created":"2023-04-12T01:04:04.948Z","updated":"2023-04-12T01:04:04.948Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":113997,"end":114157},{"type":"TextQuoteSelector","exact":"Floating point addition takes 2 - 6 clock cycles, depending on the microprocessor. Multiplication takes 3 - 8 clock cycles. Division takes 14 - 45 clock cycles.","prefix":"P16 instruction set extension.  ","suffix":" Floating point comparisons and "}]}]}
>```
>%%
>*%%PREFIX%%P16 instruction set extension.%%HIGHLIGHT%% ==Floating point addition takes 2 - 6 clock cycles, depending on the microprocessor. Multiplication takes 3 - 8 clock cycles. Division takes 14 - 45 clock cycles.== %%POSTFIX%%Floating point comparisons and*
>%%LINK%%[[#^ecn1gptoxa|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^ecn1gptoxa


>%%
>```annotation-json
>{"created":"2023-04-12T01:04:29.392Z","updated":"2023-04-12T01:04:29.392Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":114297,"end":114358},{"type":"TextQuoteSelector","exact":"Do not mix single and double precision in the same expression","prefix":"ing point registers are used.   ","suffix":". See page 153.  Avoid conversio"}]}]}
>```
>%%
>*%%PREFIX%%ing point registers are used.%%HIGHLIGHT%% ==Do not mix single and double precision in the same expression== %%POSTFIX%%. See page 153.  Avoid conversio*
>%%LINK%%[[#^mhf19yog5yb|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^mhf19yog5yb


>%%
>```annotation-json
>{"created":"2023-04-12T01:04:40.432Z","updated":"2023-04-12T01:04:40.432Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":114375,"end":114439},{"type":"TextQuoteSelector","exact":"Avoid conversions between integers and floating point variables,","prefix":"same expression. See page 153.  ","suffix":" if possible. See page 153.  App"}]}]}
>```
>%%
>*%%PREFIX%%same expression. See page 153.%%HIGHLIGHT%% ==Avoid conversions between integers and floating point variables,== %%POSTFIX%%if possible. See page 153.  App*
>%%LINK%%[[#^4c39kpafo5x|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^4c39kpafo5x


>%%
>```annotation-json
>{"created":"2023-04-12T01:05:13.547Z","updated":"2023-04-12T01:05:13.547Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":114468,"end":114650},{"type":"TextQuoteSelector","exact":"Applications that generate floating point underflow in vector registers can benefit from setting the flush-to-zero mode rather than generating subnormal numbers in case of underflow:","prefix":"es, if possible. See page 153.  ","suffix":"  // Example 7.5. Set flush-to-z"}]}]}
>```
>%%
>*%%PREFIX%%es, if possible. See page 153.%%HIGHLIGHT%% ==Applications that generate floating point underflow in vector registers can benefit from setting the flush-to-zero mode rather than generating subnormal numbers in case of underflow:== %%POSTFIX%%// Example 7.5. Set flush-to-z*
>%%LINK%%[[#^154ctc3d7pp|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^154ctc3d7pp


>%%
>```annotation-json
>{"created":"2023-04-12T01:05:28.819Z","updated":"2023-04-12T01:05:28.819Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":114770,"end":114883},{"type":"TextQuoteSelector","exact":"It is strongly recommended to set the flush-to-zero mode unless you have special reasons to use subnormal numbers","prefix":"O_MODE(_MM_FLUSH_ZERO_ON);  33  ","suffix":". You may, in addition, set the "}]}]}
>```
>%%
>*%%PREFIX%%O_MODE(_MM_FLUSH_ZERO_ON);  33%%HIGHLIGHT%% ==It is strongly recommended to set the flush-to-zero mode unless you have special reasons to use subnormal numbers== %%POSTFIX%%. You may, in addition, set the*
>%%LINK%%[[#^erwwm3ftbgk|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^erwwm3ftbgk


>%%
>```annotation-json
>{"created":"2023-04-12T01:07:16.727Z","updated":"2023-04-12T01:07:16.727Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":115377,"end":115481},{"type":"TextQuoteSelector","exact":"Enums in header files should therefore have long and unique enumerator names or be put into a namespace.","prefix":" function having the same name. ","suffix":"  7.5 Booleans The order of Bool"}]}]}
>```
>%%
>*%%PREFIX%%function having the same name.%%HIGHLIGHT%% ==Enums in header files should therefore have long and unique enumerator names or be put into a namespace.== %%POSTFIX%%7.5 Booleans The order of Bool*
>%%LINK%%[[#^jgoie060z7|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^jgoie060z7


>%%
>```annotation-json
>{"created":"2023-04-12T01:10:30.285Z","updated":"2023-04-12T01:10:30.285Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":116499,"end":116593},{"type":"TextQuoteSelector","exact":"If one operand is more predictable than the other, then put the most predictable operand first","prefix":"lanation of branch prediction.  ","suffix":".   If one operand is faster to "}]}]}
>```
>%%
>*%%PREFIX%%lanation of branch prediction.%%HIGHLIGHT%% ==If one operand is more predictable than the other, then put the most predictable operand first== %%POSTFIX%%.   If one operand is faster to*
>%%LINK%%[[#^zes2ln1z31d|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^zes2ln1z31d


>%%
>```annotation-json
>{"created":"2023-04-12T01:10:43.077Z","updated":"2023-04-12T01:10:43.077Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":116597,"end":116707},{"type":"TextQuoteSelector","exact":"If one operand is faster to calculate than the other then put the operand that is calculated the fastest first","prefix":"st predictable operand first.   ","suffix":".  However, you must be careful "}]}]}
>```
>%%
>*%%PREFIX%%st predictable operand first.%%HIGHLIGHT%% ==If one operand is faster to calculate than the other then put the operand that is calculated the fastest first== %%POSTFIX%%.  However, you must be careful*
>%%LINK%%[[#^d96a4xghkdl|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^d96a4xghkdl


>%%
>```annotation-json
>{"created":"2023-04-12T01:17:44.774Z","updated":"2023-04-12T01:17:44.774Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":117554,"end":117795},{"type":"TextQuoteSelector","exact":"Boolean variables are overdetermined in the sense that all operators that have Boolean variables as input check if the inputs have any other value than 0 or 1, but operators that have Booleans as output can produce no other value than 0 or 1","prefix":"ue 0 for false and 1 for true.  ","suffix":". This makes operations with Boo"}]}]}
>```
>%%
>*%%PREFIX%%ue 0 for false and 1 for true.%%HIGHLIGHT%% ==Boolean variables are overdetermined in the sense that all operators that have Boolean variables as input check if the inputs have any other value than 0 or 1, but operators that have Booleans as output can produce no other value than 0 or 1== %%POSTFIX%%. This makes operations with Boo*
>%%LINK%%[[#^mqu6x88empg|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^mqu6x88empg


>%%
>```annotation-json
>{"created":"2023-04-12T01:17:55.304Z","updated":"2023-04-12T01:17:55.304Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":117797,"end":117880},{"type":"TextQuoteSelector","exact":"This makes operations with Boolean variables as input less efficient than necessary","prefix":"uce no other value than 0 or 1. ","suffix":". Take the example:  // Example "}]}]}
>```
>%%
>*%%PREFIX%%uce no other value than 0 or 1.%%HIGHLIGHT%% ==This makes operations with Boolean variables as input less efficient than necessary== %%POSTFIX%%. Take the example:  // Example*
>%%LINK%%[[#^iqv8ywml3q|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^iqv8ywml3q


>%%
>```annotation-json
>{"created":"2023-04-12T01:20:20.072Z","updated":"2023-04-12T01:20:20.072Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":118385,"end":118521},{"type":"TextQuoteSelector","exact":"The Boolean operations can be made much more efficient if it is known with certainty that the operands have no other values than 0 and 1","prefix":"f mispredictions (see page 43). ","suffix":". The reason why the compiler do"}]}]}
>```
>%%
>*%%PREFIX%%f mispredictions (see page 43).%%HIGHLIGHT%% ==The Boolean operations can be made much more efficient if it is known with certainty that the operands have no other values than 0 and 1== %%POSTFIX%%. The reason why the compiler do*
>%%LINK%%[[#^l7uroqmxru|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^l7uroqmxru


>%%
>```annotation-json
>{"created":"2023-04-12T01:22:47.142Z","updated":"2023-04-12T01:22:47.142Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":119090,"end":119166},{"type":"TextQuoteSelector","exact":"The bitwise operators are single instructions that take only one clock cycle","prefix":" Boolean operators (&& and ||). ","suffix":". The OR operator (|) works  35 "}]}]}
>```
>%%
>*%%PREFIX%%Boolean operators (&& and ||).%%HIGHLIGHT%% ==The bitwise operators are single instructions that take only one clock cycle== %%POSTFIX%%. The OR operator (|) works  35*
>%%LINK%%[[#^bqtr3vfjo1n|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^bqtr3vfjo1n


>%%
>```annotation-json
>{"created":"2023-04-12T01:26:22.454Z","updated":"2023-04-12T01:26:22.454Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":119650,"end":119863},{"type":"TextQuoteSelector","exact":"You cannot replace a && b with a & b if b is an expression that should not be evaluated if a is false. Likewise, you cannot replace a || b with a | b if b is an expression that should not be evaluated if a is true","prefix":".10b char a = 0, b; b = a ^ 1;  ","suffix":".  The trick of using bitwise op"}]}]}
>```
>%%
>*%%PREFIX%%.10b char a = 0, b; b = a ^ 1;%%HIGHLIGHT%% ==You cannot replace a && b with a & b if b is an expression that should not be evaluated if a is false. Likewise, you cannot replace a || b with a | b if b is an expression that should not be evaluated if a is true== %%POSTFIX%%.  The trick of using bitwise op*
>%%LINK%%[[#^plg4zwhrysd|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^plg4zwhrysd


>%%
>```annotation-json
>{"created":"2023-04-12T01:28:21.799Z","updated":"2023-04-12T01:28:21.799Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":120227,"end":120465},{"type":"TextQuoteSelector","exact":"An integer may be used as a Boolean vector. For example, if a and b are 32-bit integers, then the expression y = a & b; will make 32 AND-operations in just one clock cycle. The operators &, |, ^, ~ are useful for Boolean vector operations","prefix":"ions. Boolean vector operations ","suffix":".  7.6 Pointers and references P"}]}]}
>```
>%%
>*%%PREFIX%%ions. Boolean vector operations%%HIGHLIGHT%% ==An integer may be used as a Boolean vector. For example, if a and b are 32-bit integers, then the expression y = a & b; will make 32 AND-operations in just one clock cycle. The operators &, |, ^, ~ are useful for Boolean vector operations== %%POSTFIX%%.  7.6 Pointers and references P*
>%%LINK%%[[#^9lzj9k6gkzk|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^9lzj9k6gkzk


>%%
>```annotation-json
>{"created":"2023-04-12T03:36:08.917Z","updated":"2023-04-12T03:36:08.917Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":120523,"end":120614},{"type":"TextQuoteSelector","exact":"Pointers and references are equally efficient because they are in fact doing the same thing","prefix":"nces Pointers versus references ","suffix":". Example:  // Example 7.12 void"}]}]}
>```
>%%
>*%%PREFIX%%nces Pointers versus references%%HIGHLIGHT%% ==Pointers and references are equally efficient because they are in fact doing the same thing== %%POSTFIX%%. Example:  // Example 7.12 void*
>%%LINK%%[[#^6rv60mm5nps|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^6rv60mm5nps


>%%
>```annotation-json
>{"created":"2023-04-12T03:44:23.342Z","updated":"2023-04-12T03:44:23.342Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":121408,"end":121467},{"type":"TextQuoteSelector","exact":"The advantages of using references rather than pointers are","prefix":"etic operations with pointers.  ","suffix":":  • The syntax is simpler when "}]}]}
>```
>%%
>*%%PREFIX%%etic operations with pointers.%%HIGHLIGHT%% ==The advantages of using references rather than pointers are== %%POSTFIX%%:  • The syntax is simpler when*
>%%LINK%%[[#^pntnbwlr0n9|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^pntnbwlr0n9


>%%
>```annotation-json
>{"created":"2023-04-12T03:45:33.016Z","updated":"2023-04-12T03:45:33.016Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":121829,"end":121898},{"type":"TextQuoteSelector","exact":"References are useful for copy constructors and overloaded operators.","prefix":"type-casted to a wrong type.  • ","suffix":"  • Function parameters that are"}]}]}
>```
>%%
>*%%PREFIX%%type-casted to a wrong type.  •%%HIGHLIGHT%% ==References are useful for copy constructors and overloaded operators.== %%POSTFIX%%• Function parameters that are*
>%%LINK%%[[#^i9a9ktfu8d|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^i9a9ktfu8d


>%%
>```annotation-json
>{"created":"2023-04-12T03:47:52.458Z","updated":"2023-04-12T03:47:52.458Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":122257,"end":122534},{"type":"TextQuoteSelector","exact":"All non-static variables and objects declared inside a function are stored on the stack and are in fact addressed relative to the stack pointer. Likewise, all non-static variables and objects declared in a class are accessed through the implicit pointer known in C++ as 'this'.","prefix":"icroprocessors are constructed. ","suffix":" We can therefore conclude that "}]}]}
>```
>%%
>*%%PREFIX%%icroprocessors are constructed.%%HIGHLIGHT%% ==All non-static variables and objects declared inside a function are stored on the stack and are in fact addressed relative to the stack pointer. Likewise, all non-static variables and objects declared in a class are accessed through the implicit pointer known in C++ as 'this'.== %%POSTFIX%%We can therefore conclude that*
>%%LINK%%[[#^8uqawksk5wj|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^8uqawksk5wj


>%%
>```annotation-json
>{"created":"2023-04-12T03:54:11.677Z","updated":"2023-04-12T03:54:11.677Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":122784,"end":122849},{"type":"TextQuoteSelector","exact":"However, there are disadvantages of using pointers and references","prefix":"ent, and that's what they are.  ","suffix":". Most importantly, it requires "}]}]}
>```
>%%
>*%%PREFIX%%ent, and that's what they are.%%HIGHLIGHT%% ==However, there are disadvantages of using pointers and references== %%POSTFIX%%. Most importantly, it requires*
>%%LINK%%[[#^5q6b39ftkcl|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^5q6b39ftkcl


>%%
>```annotation-json
>{"created":"2023-04-12T03:56:01.724Z","updated":"2023-04-12T03:56:01.724Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":123007,"end":123144},{"type":"TextQuoteSelector","exact":"f there are not enough registers then the pointer has to be loaded from memory each time it is used and this will make the program slower","prefix":"ce, especially in 32-bit mode. I","suffix":". Another disadvantage is that t"}]}]}
>```
>%%
>*%%PREFIX%%ce, especially in 32-bit mode. I%%HIGHLIGHT%% ==f there are not enough registers then the pointer has to be loaded from memory each time it is used and this will make the program slower== %%POSTFIX%%. Another disadvantage is that t*
>%%LINK%%[[#^v4nr9brfk8r|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^v4nr9brfk8r


>%%
>```annotation-json
>{"created":"2023-04-13T00:22:53.725Z","updated":"2023-04-13T00:22:53.725Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":123452,"end":123555},{"type":"TextQuoteSelector","exact":"When an integer is added to a pointer then its value is multiplied by the size of the object pointed to","prefix":" integer arithmetic operations. ","suffix":". For example:  // Example 7.13 "}]}]}
>```
>%%
>*%%PREFIX%%integer arithmetic operations.%%HIGHLIGHT%% ==When an integer is added to a pointer then its value is multiplied by the size of the object pointed to== %%POSTFIX%%. For example:  // Example 7.13*
>%%LINK%%[[#^bd6qp6sm42|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^bd6qp6sm42


>%%
>```annotation-json
>{"created":"2023-04-13T00:28:33.551Z","updated":"2023-04-13T00:28:33.551Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":124561,"end":124658},{"type":"TextQuoteSelector","exact":"Therefore, it is recommended to calculate the value of a pointer well before the pointer is used.","prefix":"he pointer has been calculated. ","suffix":" For example, x = *(p++) is more"}]}]}
>```
>%%
>*%%PREFIX%%he pointer has been calculated.%%HIGHLIGHT%% ==Therefore, it is recommended to calculate the value of a pointer well before the pointer is used.== %%POSTFIX%%For example, x = *(p++) is more*
>%%LINK%%[[#^r28v41bg3vs|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^r28v41bg3vs


>%%
>```annotation-json
>{"created":"2023-04-13T00:29:28.171Z","updated":"2023-04-13T00:29:28.171Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":124999,"end":125151},{"type":"TextQuoteSelector","exact":"Calling a function through a function pointer may take a few clock cycles more than calling the function directly if the target address can be predicted","prefix":"erators.  7.7 Function pointers ","suffix":". The target address is predicte"}]}]}
>```
>%%
>*%%PREFIX%%erators.  7.7 Function pointers%%HIGHLIGHT%% ==Calling a function through a function pointer may take a few clock cycles more than calling the function directly if the target address can be predicted== %%POSTFIX%%. The target address is predicte*
>%%LINK%%[[#^lhr911rewvl|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^lhr911rewvl


>%%
>```annotation-json
>{"created":"2023-04-13T00:31:28.265Z","updated":"2023-04-13T00:31:28.265Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":125470,"end":125666},{"type":"TextQuoteSelector","exact":"In simple cases, a data member pointer simply stores the offset of a data member relative to the beginning of the object, and a member function pointer is simply the address of the member function","prefix":"ediction.   7.8 Member pointers ","suffix":". But there are special cases su"}]}]}
>```
>%%
>*%%PREFIX%%ediction.   7.8 Member pointers%%HIGHLIGHT%% ==In simple cases, a data member pointer simply stores the offset of a data member relative to the beginning of the object, and a member function pointer is simply the address of the member function== %%POSTFIX%%. But there are special cases su*
>%%LINK%%[[#^xgu9w3xtg3s|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^xgu9w3xtg3s


>%%
>```annotation-json
>{"created":"2023-04-13T00:32:28.242Z","updated":"2023-04-13T00:32:28.242Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":126496,"end":126766},{"type":"TextQuoteSelector","exact":"Most C++ compilers have various options to control the way member pointers are implemented. Use the option that gives the simplest possible implementation if possible, and make sure you are using the same compiler option for all modules that use the same member pointer.","prefix":"ember pointers less efficient.  ","suffix":"  7.9 Smart pointers A smart poi"}]}]}
>```
>%%
>*%%PREFIX%%ember pointers less efficient.%%HIGHLIGHT%% ==Most C++ compilers have various options to control the way member pointers are implemented. Use the option that gives the simplest possible implementation if possible, and make sure you are using the same compiler option for all modules that use the same member pointer.== %%POSTFIX%%7.9 Smart pointers A smart poi*
>%%LINK%%[[#^0kp3cb3rouq|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^0kp3cb3rouq


>%%
>```annotation-json
>{"created":"2023-04-13T00:33:46.412Z","updated":"2023-04-13T00:33:46.412Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":127646,"end":127715},{"type":"TextQuoteSelector","exact":"There is no extra cost to accessing an object through a smart pointer","prefix":"e pointers to the same object.  ","suffix":". Accessing an object by *p or p"}]}]}
>```
>%%
>*%%PREFIX%%e pointers to the same object.%%HIGHLIGHT%% ==There is no extra cost to accessing an object through a smart pointer== %%POSTFIX%%. Accessing an object by *p or p*
>%%LINK%%[[#^g2gjvf0rg0f|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^g2gjvf0rg0f


>%%
>```annotation-json
>{"created":"2023-04-13T00:34:12.322Z","updated":"2023-04-13T00:34:12.322Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":127822,"end":128007},{"type":"TextQuoteSelector","exact":"But there is an extra cost whenever a smart pointer is created, deleted, copied, or transferred from one function to another. These costs are higher for shared_ptr than for unique_ptr. ","prefix":"ple pointer or a smart pointer. ","suffix":" The best optimizing compilers ("}]}]}
>```
>%%
>*%%PREFIX%%ple pointer or a smart pointer.%%HIGHLIGHT%% ==But there is an extra cost whenever a smart pointer is created, deleted, copied, or transferred from one function to another. These costs are higher for shared_ptr than for unique_ptr.== %%POSTFIX%%The best optimizing compilers (*
>%%LINK%%[[#^4minveo7nct|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^4minveo7nct


>%%
>```annotation-json
>{"created":"2023-04-13T00:35:14.744Z","updated":"2023-04-13T00:35:14.744Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":128203,"end":128476},{"type":"TextQuoteSelector","exact":"Smart pointers can be useful in the situation where the logic structure of a program dictates that an object must be dynamically created by one function and later deleted by another function and these two functions are unrelated to each other (not member of the same class)","prefix":"t the calls to new and delete.  ","suffix":". If the same function or class "}]}]}
>```
>%%
>*%%PREFIX%%t the calls to new and delete.%%HIGHLIGHT%% ==Smart pointers can be useful in the situation where the logic structure of a program dictates that an object must be dynamically created by one function and later deleted by another function and these two functions are unrelated to each other (not member of the same class)== %%POSTFIX%%. If the same function or class*
>%%LINK%%[[#^sdpnzkts5b|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^sdpnzkts5b


>%%
>```annotation-json
>{"created":"2023-04-13T00:37:10.367Z","updated":"2023-04-13T00:37:10.367Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":128599,"end":128750},{"type":"TextQuoteSelector","exact":"If a program uses many small dynamically allocated objects with each their smart pointer then you may consider if the cost of this solution is too high","prefix":"u do not need a smart pointer.  ","suffix":". It may be more efficient to po"}]}]}
>```
>%%
>*%%PREFIX%%u do not need a smart pointer.%%HIGHLIGHT%% ==If a program uses many small dynamically allocated objects with each their smart pointer then you may consider if the cost of this solution is too high== %%POSTFIX%%. It may be more efficient to po*
>%%LINK%%[[#^vbkl1p29r2f|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^vbkl1p29r2f


>%%
>```annotation-json
>{"created":"2023-04-13T01:07:11.554Z","updated":"2023-04-13T01:07:11.554Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":134111,"end":134238},{"type":"TextQuoteSelector","exact":"Conversions between signed and unsigned integers simply makes the compiler interpret the bits of the integer in a different way","prefix":"f ((unsigned int)i < 10) { ...  ","suffix":". There is no checking for overf"}]}]}
>```
>%%
>*%%PREFIX%%f ((unsigned int)i < 10) { ...%%HIGHLIGHT%% ==Conversions between signed and unsigned integers simply makes the compiler interpret the bits of the integer in a different way== %%POSTFIX%%. There is no checking for overf*
>%%LINK%%[[#^7wyyb72pb4f|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^7wyyb72pb4f


>%%
>```annotation-json
>{"created":"2023-04-13T01:09:56.238Z","updated":"2023-04-13T01:09:56.238Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":135215,"end":135331},{"type":"TextQuoteSelector","exact":"Conversions between float, double and long double take no extra time when the floating point register stack is used.","prefix":"ting point precision conversion ","suffix":" It takes between 2 and 15 clock"}]}]}
>```
>%%
>*%%PREFIX%%ting point precision conversion%%HIGHLIGHT%% ==Conversions between float, double and long double take no extra time when the floating point register stack is used.== %%POSTFIX%%It takes between 2 and 15 clock*
>%%LINK%%[[#^ua8cgdx93rs|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^ua8cgdx93rs


>%%
>```annotation-json
>{"created":"2023-04-13T01:10:17.356Z","updated":"2023-04-13T01:10:17.356Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":135332,"end":135431},{"type":"TextQuoteSelector","exact":"It takes between 2 and 15 clock cycles (depending on the processor) when the XMM registers are used","prefix":"g point register stack is used. ","suffix":". See page 31 for an explanation"}]}]}
>```
>%%
>*%%PREFIX%%g point register stack is used.%%HIGHLIGHT%% ==It takes between 2 and 15 clock cycles (depending on the processor) when the XMM registers are used== %%POSTFIX%%. See page 31 for an explanation*
>%%LINK%%[[#^odwtpxv3tmb|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^odwtpxv3tmb


>%%
>```annotation-json
>{"created":"2023-04-13T01:10:59.253Z","updated":"2023-04-13T01:10:59.253Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":135742,"end":135819},{"type":"TextQuoteSelector","exact":"Conversion of a signed integer to a float or double takes 4 - 16 clock cycles","prefix":"on. Integer to float conversion ","suffix":", depending on the processor and"}]}]}
>```
>%%
>*%%PREFIX%%on. Integer to float conversion%%HIGHLIGHT%% ==Conversion of a signed integer to a float or double takes 4 - 16 clock cycles== %%POSTFIX%%, depending on the processor and*
>%%LINK%%[[#^kfw0951tnms|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^kfw0951tnms


>%%
>```annotation-json
>{"created":"2023-04-13T01:11:35.710Z","updated":"2023-04-13T01:11:35.710Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":135880,"end":136140},{"type":"TextQuoteSelector","exact":"Conversion of unsigned integers takes longer time than signed integers unless the AVX512 instruction set is enabled (AVX512DQ for 64 bit unsigned integers). It is faster to first convert the unsigned integer to a signed integer if there is no risk of overflow:","prefix":"and the type of registers used. ","suffix":"  // Example 7.25 unsigned int u"}]}]}
>```
>%%
>*%%PREFIX%%and the type of registers used.%%HIGHLIGHT%% ==Conversion of unsigned integers takes longer time than signed integers unless the AVX512 instruction set is enabled (AVX512DQ for 64 bit unsigned integers). It is faster to first convert the unsigned integer to a signed integer if there is no risk of overflow:== %%POSTFIX%%// Example 7.25 unsigned int u*
>%%LINK%%[[#^4o6hzn9co42|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^4o6hzn9co42


>%%
>```annotation-json
>{"created":"2023-04-13T01:31:37.505Z","updated":"2023-04-13T01:31:37.505Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":136246,"end":136362},{"type":"TextQuoteSelector","exact":"Integer to float conversions can sometimes be avoided by replacing an integer variable by a float variable. Example:","prefix":"/ Faster, but risk of overflow  ","suffix":"  // Example 7.26a float a[100];"}]}]}
>```
>%%
>*%%PREFIX%%/ Faster, but risk of overflow%%HIGHLIGHT%% ==Integer to float conversions can sometimes be avoided by replacing an integer variable by a float variable. Example:== %%POSTFIX%%// Example 7.26a float a[100];*
>%%LINK%%[[#^65b6zmwrokm|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^65b6zmwrokm


>%%
>```annotation-json
>{"created":"2023-04-13T01:32:20.625Z","updated":"2023-04-13T01:32:20.625Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":136693,"end":136821},{"type":"TextQuoteSelector","exact":"Conversion of a floating point number to an integer takes a very long time unless the SSE2 or later instruction set is enabled. ","prefix":"i2; Float to integer conversion ","suffix":"Typically, the conversion takes "}]}]}
>```
>%%
>*%%PREFIX%%i2; Float to integer conversion%%HIGHLIGHT%% ==Conversion of a floating point number to an integer takes a very long time unless the SSE2 or later instruction set is enabled.== %%POSTFIX%%Typically, the conversion takes*
>%%LINK%%[[#^hh7xfwp2hhn|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^hh7xfwp2hhn


>%%
>```annotation-json
>{"created":"2023-04-13T01:32:40.410Z","updated":"2023-04-13T01:32:40.410Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":136821,"end":137017},{"type":"TextQuoteSelector","exact":"Typically, the conversion takes 50 - 100 clock cycles. The reason is that the C/C++ standard specifies truncation so the floating point rounding mode has to be changed to truncation and back again","prefix":"ter instruction set is enabled. ","suffix":".   If there are floating point-"}]}]}
>```
>%%
>*%%PREFIX%%ter instruction set is enabled.%%HIGHLIGHT%% ==Typically, the conversion takes 50 - 100 clock cycles. The reason is that the C/C++ standard specifies truncation so the floating point rounding mode has to be changed to truncation and back again== %%POSTFIX%%.   If there are floating point-*
>%%LINK%%[[#^rp1gptyelrk|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^rp1gptyelrk


>%%
>```annotation-json
>{"created":"2023-04-13T01:35:29.553Z","updated":"2023-04-13T01:35:29.553Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":137021,"end":137148},{"type":"TextQuoteSelector","exact":"If there are floating point-to-integer conversions in the critical part of a code then it is important to do something about it","prefix":"to truncation and back again.   ","suffix":". Possible solutions are:  Avoid"}]}]}
>```
>%%
>*%%PREFIX%%to truncation and back again.%%HIGHLIGHT%% ==If there are floating point-to-integer conversions in the critical part of a code then it is important to do something about it== %%POSTFIX%%. Possible solutions are:  Avoid*
>%%LINK%%[[#^nxhnh9b1l1q|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^nxhnh9b1l1q


>%%
>```annotation-json
>{"created":"2023-04-13T01:43:47.929Z","updated":"2023-04-13T01:43:47.929Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":138902,"end":138974},{"type":"TextQuoteSelector","exact":"There are a number of dangers to be aware of when type-casting pointers:","prefix":" is faster than x = -abs(x);.   ","suffix":"  • The trick violates the stric"}]}]}
>```
>%%
>*%%PREFIX%%is faster than x = -abs(x);.%%HIGHLIGHT%% ==There are a number of dangers to be aware of when type-casting pointers:== %%POSTFIX%%• The trick violates the stric*
>%%LINK%%[[#^djioty9hiop|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^djioty9hiop


>%%
>```annotation-json
>{"created":"2023-04-13T01:46:39.457Z","updated":"2023-04-13T01:46:39.457Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":139992,"end":140075},{"type":"TextQuoteSelector","exact":"The const_cast operator is used for relieving the const restriction from a pointer.","prefix":" AMD and VIA CPUs\"). Const cast ","suffix":" It has some syntax checking and"}]}]}
>```
>%%
>*%%PREFIX%%AMD and VIA CPUs"). Const cast%%HIGHLIGHT%% ==The const_cast operator is used for relieving the const restriction from a pointer.== %%POSTFIX%%It has some syntax checking and*
>%%LINK%%[[#^zbbdr9uebej|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^zbbdr9uebej


>%%
>```annotation-json
>{"created":"2023-04-13T01:47:19.488Z","updated":"2023-04-13T01:47:19.488Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":140650,"end":140747},{"type":"TextQuoteSelector","exact":"This is a useful way of making sure that one function can modify x, while other functions cannot.","prefix":"d does not take any extra time. ","suffix":" Static cast The static_cast ope"}]}]}
>```
>%%
>*%%PREFIX%%d does not take any extra time.%%HIGHLIGHT%% ==This is a useful way of making sure that one function can modify x, while other functions cannot.== %%POSTFIX%%Static cast The static_cast ope*
>%%LINK%%[[#^am403slwm17|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^am403slwm17


>%%
>```annotation-json
>{"created":"2023-04-13T01:48:41.608Z","updated":"2023-04-13T01:48:41.608Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":140895,"end":140956},{"type":"TextQuoteSelector","exact":"The reinterpret_cast operator is used for pointer conversions","prefix":" float to int. Reinterpret cast ","suffix":". It does the same as C-style ty"}]}]}
>```
>%%
>*%%PREFIX%%float to int. Reinterpret cast%%HIGHLIGHT%% ==The reinterpret_cast operator is used for pointer conversions== %%POSTFIX%%. It does the same as C-style ty*
>%%LINK%%[[#^h3gezjjxcwd|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^h3gezjjxcwd


>%%
>```annotation-json
>{"created":"2023-04-13T01:49:01.479Z","updated":"2023-04-13T01:49:01.479Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":141081,"end":141182},{"type":"TextQuoteSelector","exact":"The dynamic_cast operator is used for converting a pointer to one class to a pointer to another class","prefix":"ce any extra code. Dynamic cast ","suffix":". It makes a runtime check that "}]}]}
>```
>%%
>*%%PREFIX%%ce any extra code. Dynamic cast%%HIGHLIGHT%% ==The dynamic_cast operator is used for converting a pointer to one class to a pointer to another class== %%POSTFIX%%. It makes a runtime check that*
>%%LINK%%[[#^oabw5nsn1kd|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^oabw5nsn1kd


>%%
>```annotation-json
>{"created":"2023-04-17T00:39:28.941Z","updated":"2023-04-17T00:39:28.941Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":142890,"end":143137},{"type":"TextQuoteSelector","exact":"Modern microprocessors are using advanced algorithms to predict which way a branch will go based on the past history of that branch and other nearby branches. The algorithms used for branch prediction are different for each type of microprocessor.","prefix":"t is used is branch prediction. ","suffix":" These algorithms are described "}]}]}
>```
>%%
>*%%PREFIX%%t is used is branch prediction.%%HIGHLIGHT%% ==Modern microprocessors are using advanced algorithms to predict which way a branch will go based on the past history of that branch and other nearby branches. The algorithms used for branch prediction are different for each type of microprocessor.== %%POSTFIX%%These algorithms are described*
>%%LINK%%[[#^z5c8k6vv7ri|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^z5c8k6vv7ri


>%%
>```annotation-json
>{"created":"2023-04-17T00:44:36.540Z","updated":"2023-04-17T00:44:36.540Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":143245,"end":143539},{"type":"TextQuoteSelector","exact":"A branch instruction takes typically 0 - 2 clock cycles in the case that the microprocessor has made the right prediction. The time it takes to recover from a branch misprediction is approximately 12 - 25 clock cycles, depending on the processor. This is called the branch misprediction penalty","prefix":"e of Intel, AMD and VIA CPUs\".  ","suffix":".  Branches are relatively cheap"}]}]}
>```
>%%
>*%%PREFIX%%e of Intel, AMD and VIA CPUs".%%HIGHLIGHT%% ==A branch instruction takes typically 0 - 2 clock cycles in the case that the microprocessor has made the right prediction. The time it takes to recover from a branch misprediction is approximately 12 - 25 clock cycles, depending on the processor. This is called the branch misprediction penalty== %%POSTFIX%%.  Branches are relatively cheap*
>%%LINK%%[[#^d21je3jq41k|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^d21je3jq41k


>%%
>```annotation-json
>{"created":"2023-04-17T00:49:03.231Z","updated":"2023-04-17T00:49:03.231Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":144886,"end":145147},{"type":"TextQuoteSelector","exact":"A switch statements is a kind of branch that can go more than two ways. Switch statements are most efficient if the case labels follow a sequence where each label is equal to the preceding label plus one, because it can be implemented as a table of jump targets","prefix":"ranches is not predicted well.  ","suffix":". A switch statement with many l"}]}]}
>```
>%%
>*%%PREFIX%%ranches is not predicted well.%%HIGHLIGHT%% ==A switch statements is a kind of branch that can go more than two ways. Switch statements are most efficient if the case labels follow a sequence where each label is equal to the preceding label plus one, because it can be implemented as a table of jump targets== %%POSTFIX%%. A switch statement with many l*
>%%LINK%%[[#^wbxoeoz3o7g|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^wbxoeoz3o7g


>%%
>```annotation-json
>{"created":"2023-04-17T00:49:17.906Z","updated":"2023-04-17T00:49:17.906Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":145149,"end":145290},{"type":"TextQuoteSelector","exact":"A switch statement with many labels that have values far from each other is inefficient because the compiler must convert it to a branch tree","prefix":"ted as a table of jump targets. ","suffix":".  On older processors, a switch"}]}]}
>```
>%%
>*%%PREFIX%%ted as a table of jump targets.%%HIGHLIGHT%% ==A switch statement with many labels that have values far from each other is inefficient because the compiler must convert it to a branch tree== %%POSTFIX%%.  On older processors, a switch*
>%%LINK%%[[#^502dxfrlr7l|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^502dxfrlr7l


>%%
>```annotation-json
>{"created":"2023-04-17T00:51:45.361Z","updated":"2023-04-17T00:51:45.361Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":145713,"end":145943},{"type":"TextQuoteSelector","exact":"The number of branches and switch statements should preferably be kept small in the critical part of a program, especially if the branches are poorly predictable. It may be useful to roll out a loop if this can eliminate branches,","prefix":"of different targets is small.  ","suffix":" as explained in the next paragr"}]}]}
>```
>%%
>*%%PREFIX%%of different targets is small.%%HIGHLIGHT%% ==The number of branches and switch statements should preferably be kept small in the critical part of a program, especially if the branches are poorly predictable. It may be useful to roll out a loop if this can eliminate branches,== %%POSTFIX%%as explained in the next paragr*
>%%LINK%%[[#^unrff7e7yy|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^unrff7e7yy


>%%
>```annotation-json
>{"created":"2023-04-17T00:52:03.086Z","updated":"2023-04-17T00:52:03.086Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":145981,"end":146084},{"type":"TextQuoteSelector","exact":"The target of branches and function calls are saved in a special cache called the branch target buffer.","prefix":"plained in the next paragraph.  ","suffix":" Contentions in the branch targe"}]}]}
>```
>%%
>*%%PREFIX%%plained in the next paragraph.%%HIGHLIGHT%% ==The target of branches and function calls are saved in a special cache called the branch target buffer.== %%POSTFIX%%Contentions in the branch targe*
>%%LINK%%[[#^l6lztetevc|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^l6lztetevc


>%%
>```annotation-json
>{"created":"2023-04-17T00:55:11.886Z","updated":"2023-04-17T00:55:11.886Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":147026,"end":147109},{"type":"TextQuoteSelector","exact":"In some cases the compiler can automatically replace a branch by a conditional move","prefix":"lues than 0 or 1. See page 34.  ","suffix":".   45 The examples on page 147 "}]}]}
>```
>%%
>*%%PREFIX%%lues than 0 or 1. See page 34.%%HIGHLIGHT%% ==In some cases the compiler can automatically replace a branch by a conditional move== %%POSTFIX%%.   45 The examples on page 147*
>%%LINK%%[[#^tquv868hiw|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^tquv868hiw


>%%
>```annotation-json
>{"created":"2023-04-17T01:03:27.078Z","updated":"2023-04-17T01:03:27.078Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":147864,"end":147994},{"type":"TextQuoteSelector","exact":"On other processors, only the innermost loop is predicted well. A loop with a high repeat count is mispredicted only when it exits","prefix":" have a special loop predictor. ","suffix":". For example, if a loop repeats"}]}]}
>```
>%%
>*%%PREFIX%%have a special loop predictor.%%HIGHLIGHT%% ==On other processors, only the innermost loop is predicted well. A loop with a high repeat count is mispredicted only when it exits== %%POSTFIX%%. For example, if a loop repeats*
>%%LINK%%[[#^zn2195dhy7m|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^zn2195dhy7m


>%%
>```annotation-json
>{"created":"2023-04-17T01:04:39.364Z","updated":"2023-04-17T01:04:39.364Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":148652,"end":148677},{"type":"TextQuoteSelector","exact":"This has three advantages","prefix":"  FuncB(i+1);    FuncC(i+1); }  ","suffix":":  • The i<20 loop control branc"}]}]}
>```
>%%
>*%%PREFIX%%FuncB(i+1);    FuncC(i+1); }%%HIGHLIGHT%% ==This has three advantages== %%POSTFIX%%:  • The i<20 loop control branc*
>%%LINK%%[[#^7qc8kewoz4n|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^7qc8kewoz4n


>%%
>```annotation-json
>{"created":"2023-04-17T01:04:45.388Z","updated":"2023-04-17T01:04:45.388Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":148901,"end":148938},{"type":"TextQuoteSelector","exact":"Loop unrolling also has disadvantages","prefix":"• The if branch is eliminated.  ","suffix":":  • The unrolled loop takes up "}]}]}
>```
>%%
>*%%PREFIX%%• The if branch is eliminated.%%HIGHLIGHT%% ==Loop unrolling also has disadvantages== %%POSTFIX%%:  • The unrolled loop takes up*
>%%LINK%%[[#^7khvpqgrhnj|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^7khvpqgrhnj



>%%
>```annotation-json
>{"created":"2023-04-17T01:05:05.262Z","updated":"2023-04-17T01:05:05.262Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":148943,"end":149016},{"type":"TextQuoteSelector","exact":"The unrolled loop takes up more space in the code cache or micro-op cache","prefix":"ling also has disadvantages:  • ","suffix":".     46 • Many CPUs have a loop"}]}]}
>```
>%%
>*%%PREFIX%%ling also has disadvantages:  •%%HIGHLIGHT%% ==The unrolled loop takes up more space in the code cache or micro-op cache== %%POSTFIX%%.     46 • Many CPUs have a loop*
>%%LINK%%[[#^kocrx6gt18|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^kocrx6gt18


>%%
>```annotation-json
>{"created":"2023-04-17T01:06:44.828Z","updated":"2023-04-17T01:06:44.828Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":149449,"end":149537},{"type":"TextQuoteSelector","exact":"Loop unrolling should only be used if there are specific advantages that can be obtained","prefix":"ivisible by the unroll factor.  ","suffix":". If a loop contains floating po"}]}]}
>```
>%%
>*%%PREFIX%%ivisible by the unroll factor.%%HIGHLIGHT%% ==Loop unrolling should only be used if there are specific advantages that can be obtained== %%POSTFIX%%. If a loop contains floating po*
>%%LINK%%[[#^tqlx6wll5b8|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^tqlx6wll5b8


>%%
>```annotation-json
>{"created":"2023-04-17T01:07:16.829Z","updated":"2023-04-17T01:07:16.829Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":149539,"end":149788},{"type":"TextQuoteSelector","exact":"If a loop contains floating point calculations or vector instructions and the loop counter is an integer, then you can generally assume that the overall computation time is determined by the floating point code rather than by the loop control branch","prefix":"dvantages that can be obtained. ","suffix":". There is nothing to gain by un"}]}]}
>```
>%%
>*%%PREFIX%%dvantages that can be obtained.%%HIGHLIGHT%% ==If a loop contains floating point calculations or vector instructions and the loop counter is an integer, then you can generally assume that the overall computation time is determined by the floating point code rather than by the loop control branch== %%POSTFIX%%. There is nothing to gain by un*
>%%LINK%%[[#^insixjib8o|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^insixjib8o


>%%
>```annotation-json
>{"created":"2023-04-17T01:10:03.268Z","updated":"2023-04-17T01:10:03.268Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":149852,"end":149923},{"type":"TextQuoteSelector","exact":"Loop unrolling is useful when there is a loop-carried dependency chain,","prefix":"rolling the loop in this case.  ","suffix":" as explained on page 113.  Loop"}]}]}
>```
>%%
>*%%PREFIX%%rolling the loop in this case.%%HIGHLIGHT%% ==Loop unrolling is useful when there is a loop-carried dependency chain,== %%POSTFIX%%as explained on page 113.  Loop*
>%%LINK%%[[#^5xfegzjjwdu|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^5xfegzjjwdu


>%%
>```annotation-json
>{"created":"2023-04-17T01:13:02.273Z","updated":"2023-04-17T01:13:02.273Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":150655,"end":150747},{"type":"TextQuoteSelector","exact":"It is less efficient if the loop control branch depends on the calculations inside the loop.","prefix":"ment several iterations ahead.  ","suffix":" The following example converts "}]}]}
>```
>%%
>*%%PREFIX%%ment several iterations ahead.%%HIGHLIGHT%% ==It is less efficient if the loop control branch depends on the calculations inside the loop.== %%POSTFIX%%The following example converts*
>%%LINK%%[[#^ejfw34r7iui|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^ejfw34r7iui


>%%
>```annotation-json
>{"created":"2023-04-17T01:14:37.535Z","updated":"2023-04-17T01:14:37.535Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":150907,"end":151000},{"type":"TextQuoteSelector","exact":"If the length of the string is already known then it is more efficient to use a loop counter:","prefix":"hile (*p != 0) *(p++) |= 0x20;  ","suffix":"  // Example 7.31b char string[1"}]}]}
>```
>%%
>*%%PREFIX%%hile (*p != 0) *(p++) |= 0x20;%%HIGHLIGHT%% ==If the length of the string is already known then it is more efficient to use a loop counter:== %%POSTFIX%%// Example 7.31b char string[1*
>%%LINK%%[[#^uce9i9gn3od|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^uce9i9gn3od


>%%
>```annotation-json
>{"created":"2023-04-17T01:22:21.229Z","updated":"2023-04-17T01:22:21.229Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":152057,"end":152186},{"type":"TextQuoteSelector","exact":"A loop counter should preferably be an integer. If a loop needs a floating point counter then make an additional integer counter.","prefix":"o the total calculation time.   ","suffix":" Example:   47 // Example 7.32a "}]}]}
>```
>%%
>*%%PREFIX%%o the total calculation time.%%HIGHLIGHT%% ==A loop counter should preferably be an integer. If a loop needs a floating point counter then make an additional integer counter.== %%POSTFIX%%Example:   47 // Example 7.32a*
>%%LINK%%[[#^70olgdz8c8f|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^70olgdz8c8f


>%%
>```annotation-json
>{"created":"2023-04-17T01:22:53.244Z","updated":"2023-04-17T01:22:53.244Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":153557,"end":153614},{"type":"TextQuoteSelector","exact":"It is often faster to use the functions memset and memcpy","prefix":"0; i < size; i++) b[i] = a[i];  ","suffix":":  // Example 7.33b const int si"}]}]}
>```
>%%
>*%%PREFIX%%0; i < size; i++) b[i] = a[i];%%HIGHLIGHT%% ==It is often faster to use the functions memset and memcpy== %%POSTFIX%%:  // Example 7.33b const int si*
>%%LINK%%[[#^2fgmu7foo0p|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^2fgmu7foo0p


>%%
>```annotation-json
>{"created":"2023-04-17T01:23:04.038Z","updated":"2023-04-17T01:23:04.038Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":153764,"end":153872},{"type":"TextQuoteSelector","exact":"Most compilers will automatically replace such loops by calls to memset and memcpy, at least in simple cases","prefix":" to b memcpy(b, a, sizeof(b));  ","suffix":". The explicit use of memset and"}]}]}
>```
>%%
>*%%PREFIX%%to b memcpy(b, a, sizeof(b));%%HIGHLIGHT%% ==Most compilers will automatically replace such loops by calls to memset and memcpy, at least in simple cases== %%POSTFIX%%. The explicit use of memset and*
>%%LINK%%[[#^c2zr4syxcqb|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^c2zr4syxcqb


>%%
>```annotation-json
>{"created":"2023-04-17T01:23:46.408Z","updated":"2023-04-17T01:23:46.408Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":154108,"end":154173},{"type":"TextQuoteSelector","exact":"Function calls may slow down a program for the following reasons:","prefix":"unt is too big.  7.14 Functions ","suffix":"  • The function call makes the "}]}]}
>```
>%%
>*%%PREFIX%%unt is too big.  7.14 Functions%%HIGHLIGHT%% ==Function calls may slow down a program for the following reasons:== %%POSTFIX%%• The function call makes the*
>%%LINK%%[[#^4yt2ndllx0c|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^4yt2ndllx0c


>%%
>```annotation-json
>{"created":"2023-04-17T01:26:38.128Z","updated":"2023-04-17T01:26:38.128Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":154429,"end":154466},{"type":"TextQuoteSelector","exact":"The code cache works less efficiently","prefix":"r calculations to save time.  • ","suffix":" if the code is fragmented and s"}]}]}
>```
>%%
>*%%PREFIX%%r calculations to save time.  •%%HIGHLIGHT%% ==The code cache works less efficiently== %%POSTFIX%%if the code is fragmented and s*
>%%LINK%%[[#^k0e3m0g2qzp|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^k0e3m0g2qzp


>%%
>```annotation-json
>{"created":"2023-04-17T01:26:46.887Z","updated":"2023-04-17T01:26:46.887Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":154177,"end":154267},{"type":"TextQuoteSelector","exact":"The function call makes the microprocessor jump to a different code address and back again","prefix":"m for the following reasons:  • ","suffix":". This may take up to 4 clock cy"}]}]}
>```
>%%
>*%%PREFIX%%m for the following reasons:  •%%HIGHLIGHT%% ==The function call makes the microprocessor jump to a different code address and back again== %%POSTFIX%%. This may take up to 4 clock cy*
>%%LINK%%[[#^medf4xz91ub|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^medf4xz91ub


>%%
>```annotation-json
>{"created":"2023-04-17T01:27:17.659Z","updated":"2023-04-17T01:27:17.659Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":154532,"end":154590},{"type":"TextQuoteSelector","exact":"Function parameters are stored on the stack in 32-bit mode","prefix":"ttered around in memory.   48 • ","suffix":". Storing the parameters on the "}]}]}
>```
>%%
>*%%PREFIX%%ttered around in memory.   48 •%%HIGHLIGHT%% ==Function parameters are stored on the stack in 32-bit mode== %%POSTFIX%%. Storing the parameters on the*
>%%LINK%%[[#^e2yfq2rc5nl|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^e2yfq2rc5nl


>%%
>```annotation-json
>{"created":"2023-04-17T01:27:33.207Z","updated":"2023-04-17T01:27:33.207Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":154752,"end":154801},{"type":"TextQuoteSelector","exact":"Extra time is needed for setting up a stack frame","prefix":"a critical dependency chain.  • ","suffix":", saving and restoring registers"}]}]}
>```
>%%
>*%%PREFIX%%a critical dependency chain.  •%%HIGHLIGHT%% ==Extra time is needed for setting up a stack frame== %%POSTFIX%%, saving and restoring registers*
>%%LINK%%[[#^lshjzffghif|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^lshjzffghif


>%%
>```annotation-json
>{"created":"2023-04-17T01:27:48.166Z","updated":"2023-04-17T01:27:48.166Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":154888,"end":154967},{"type":"TextQuoteSelector","exact":"Each function call statement occupies a space in the branch target buffer (BTB)","prefix":"eption handling information.  • ","suffix":". Contentions in the BTB can cau"}]}]}
>```
>%%
>*%%PREFIX%%eption handling information.  •%%HIGHLIGHT%% ==Each function call statement occupies a space in the branch target buffer (BTB)== %%POSTFIX%%. Contentions in the BTB can cau*
>%%LINK%%[[#^ixobbgmgdxh|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^ixobbgmgdxh


>%%
>```annotation-json
>{"created":"2023-04-17T01:30:49.815Z","updated":"2023-04-17T01:30:49.815Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":155391,"end":155485},{"type":"TextQuoteSelector","exact":"Splitting up a function into multiple smaller functions only makes the program less efficient.","prefix":"ons. I disagree with this rule. ","suffix":" Splitting up a function just be"}]}]}
>```
>%%
>*%%PREFIX%%ons. I disagree with this rule.%%HIGHLIGHT%% ==Splitting up a function into multiple smaller functions only makes the program less efficient.== %%POSTFIX%%Splitting up a function just be*
>%%LINK%%[[#^1g6vb0oi04|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^1g6vb0oi04


>%%
>```annotation-json
>{"created":"2023-04-17T01:34:45.342Z","updated":"2023-04-17T01:34:45.342Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":156510,"end":156524},{"type":"TextQuoteSelector","exact":" leaf function","prefix":"l any other function is called a","suffix":". Leaf functions are more effici"}]}]}
>```
>%%
>*%%PREFIX%%l any other function is called a%%HIGHLIGHT%% ==leaf function== %%POSTFIX%%. Leaf functions are more effici*
>%%LINK%%[[#^o2959c57tse|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^o2959c57tse


>%%
>```annotation-json
>{"created":"2023-04-17T01:34:49.120Z","updated":"2023-04-17T01:34:49.120Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":156428,"end":156443},{"type":"TextQuoteSelector","exact":"frame function,","prefix":"lls other functions is called a ","suffix":" while a function that does not "}]}]}
>```
>%%
>*%%PREFIX%%lls other functions is called a%%HIGHLIGHT%% ==frame function,== %%POSTFIX%%while a function that does not*
>%%LINK%%[[#^trmz4th1bf|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^trmz4th1bf


>%%
>```annotation-json
>{"created":"2023-04-17T01:37:06.367Z","updated":"2023-04-17T01:37:06.367Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":156526,"end":156614},{"type":"TextQuoteSelector","exact":"Leaf functions are more efficient than frame functions for reasons explained on page 63.","prefix":"tion is called a leaf function. ","suffix":" If the critical innermost loop "}]}]}
>```
>%%
>*%%PREFIX%%tion is called a leaf function.%%HIGHLIGHT%% ==Leaf functions are more efficient than frame functions for reasons explained on page 63.== %%POSTFIX%%If the critical innermost loop*
>%%LINK%%[[#^gbeefg9qdr8|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^gbeefg9qdr8


>%%
>```annotation-json
>{"created":"2023-04-17T01:37:23.786Z","updated":"2023-04-17T01:37:23.786Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":156894,"end":157021},{"type":"TextQuoteSelector","exact":"A macro declared with #define is certain to be inlined. But beware that macro parameters are evaluated every time they are used","prefix":"Use macros instead of functions ","suffix":". Example:  // Example 7.34a. Us"}]}]}
>```
>%%
>*%%PREFIX%%Use macros instead of functions%%HIGHLIGHT%% ==A macro declared with #define is certain to be inlined. But beware that macro parameters are evaluated every time they are used== %%POSTFIX%%. Example:  // Example 7.34a. Us*
>%%LINK%%[[#^lho9cmh2hqa|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^lho9cmh2hqa


>%%
>```annotation-json
>{"created":"2023-04-17T01:39:02.353Z","updated":"2023-04-17T01:39:02.353Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":157529,"end":157614},{"type":"TextQuoteSelector","exact":"Another problem with macros is that the name cannot be overloaded or limited in scope","prefix":"   return a > b ? a : b; }  49  ","suffix":". A macro will interfere with an"}]}]}
>```
>%%
>*%%PREFIX%%return a > b ? a : b; }  49%%HIGHLIGHT%% ==Another problem with macros is that the name cannot be overloaded or limited in scope== %%POSTFIX%%. A macro will interfere with an*
>%%LINK%%[[#^az912r6tg9p|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^az912r6tg9p


>%%
>```annotation-json
>{"created":"2023-04-17T01:41:18.354Z","updated":"2023-04-17T01:41:18.354Z","document":{"title":"Optimizing software in C++","link":[{"href":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7"}],"documentFingerprint":"45252bb354535a499741f01ba5fe33f7"},"uri":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","target":[{"source":"urn:x-pdf:45252bb354535a499741f01ba5fe33f7","selector":[{"type":"TextPositionSelector","start":157616,"end":157820},{"type":"TextQuoteSelector","exact":"A macro will interfere with any function or variable having the same name, regardless of scope or namespaces. Therefore, it is important to use long and unique names for macros, especially in header files","prefix":"overloaded or limited in scope. ","suffix":". Use fastcall and vectorcall fu"}]}]}
>```
>%%
>*%%PREFIX%%overloaded or limited in scope.%%HIGHLIGHT%% ==A macro will interfere with any function or variable having the same name, regardless of scope or namespaces. Therefore, it is important to use long and unique names for macros, especially in header files== %%POSTFIX%%. Use fastcall and vectorcall fu*
>%%LINK%%[[#^x8o3unxddn|show annotation]]
>%%COMMENT%%
>
>%%TAGS%%
>
^x8o3unxddn
