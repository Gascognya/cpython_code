3 中 沒找到PyIntObject 
3中long和int合并了，详见
longintrepr.h -> _longobject
longobject.h -> typedef struct _longobject PyLongObject;

AOL(Abstract Object Layer) 抽象对象API
COL(Concrete Object Layer) 实体对象API

GC：
Py_INCREF(op) 增加GC
Py_DECREF(op) 减少GC，当on_refcnt为0，调用对象的tp_dealloc
对象指向类型的指针不会视为引用。

对象分类
Fundamental类型对象(type)
Numeric数值对象(integer, float, boolean)
Sequence序列对象(string, list, tuple)
Mapping对象(dict)
Internal内部对象(function, code, frame, module, method)

