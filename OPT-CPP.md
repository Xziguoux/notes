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
