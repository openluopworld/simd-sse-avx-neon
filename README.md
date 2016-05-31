
### SSE

1. [__m128i]<br>
```C
typedef union __declspec(intrin_type) _CRT_ALIGN(16) __m128i {
	__int8			m128i_i8[16];
	__int16			m128i_i16[8];
	__int32			m128i_i32[4];
	__int64			m128i_i64[2];
	unsigned __int8		m128i_u8[16];
	unsigned __int16	m128i_u16[8];
	unsigned __int32	m128i_u32[4];
	unsigned __int64	m128i_u64[2];
} __m128i;

#if !defined(_CRT_ALIGN)
	#if defined(__midl)
		#define _CRT_ALIGN(x)
	#else
		#define _CRT_ALIGN(x) __declspec(align(x))
	#endif
#endif
```

[//]:
   [__m128i]: <https://github.com/joemccann/dillinger>
