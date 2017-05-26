
## [SIMD Instructions]

## SSE

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

2. SSE2
+ __m128i _mm_unpackhi_epi16 (__m128i a, __m128i b)
+ __m128i _mm_unpackhi_epi32 (__m128i a, __m128i b)
+ __m128i _mm_unpackhi_epi64 (__m128i a, __m128i b)
+ __m128i _mm_unpackhi_epi8 (__m128i a, __m128i b)
+ __m128i _mm_unpacklo_epi16 (__m128i a, __m128i b)
+ __m128i _mm_unpacklo_epi32 (__m128i a, __m128i b)
+ __m128i _mm_unpacklo_epi64 (__m128i a, __m128i b)
+ __m128i _mm_unpacklo_epi8 (__m128i a, __m128i b)

## Test supporting
```C
#include <stdio.h>
#include <emmintrin.h>

int main (void ) {

	__m128i a = _mm_set1_epi8(0x11);

	return 0;

}
```
Compile with
```sh
$ gcc -march=native test.c
```

[SIMD Instructions]:<https://software.intel.com/sites/landingpage/IntrinsicsGuide/>
