# ADT


abstract data types for the C language

* string
* array
* hash
* stack

# Example Usage

## ADT String
``` C
adt_str_t *str = adt_str_new();
adt_str_push(str,'a');
adt_str_push(str,'b');
adt_str_push(str,'c');
const char *result = adt_str_cstr(str); //returns "abc"
adt_str_delete(str);
```

## ADT Array
``` c
adt_ary_t *pArray = adt_ary_new(free);
adt_ary_push(pArray,strdup("elem1"));
char *pElem = (char*) adt_ary_pop(pArray);
adt_ary_delete(pArray);
free(pElem);
```

## ADT Hash
``` C
adt_hash_t *pHash = adt_hash_new(free);
adt_hash_set(pHash,"first",0,"The");
adt_hash_set(pHash,"second",0,"quick");
adt_hash_set(pHash,"third",0,"brown");
adt_hash_set(pHash,"fourth",0,"fox");
const char *pVal = adt_hash_get(pHash,"third",0);
```

## ADT Stack
``` C
adt_stack_t *pStack = adt_stack_new(free);
adt_stack_push(pStack,strdup("The"));
adt_stack_push(pStack,strdup("quick"));
adt_stack_push(pStack,strdup("brown"));
adt_stack_push(pStack,strdup("fox"));
const char *pVal = adt_stack_top(pStack);
adt_stack_delete(pStack);
```




