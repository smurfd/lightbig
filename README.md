## lightbig
A light bigint C implementation

### Build
```
make -Csrc
```

### Usage
```
git clone https://github.com/smurfd/lightbig
```
test_lightbig.c
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>
#include <assert.h>
#include "lightbig/src/lightbig.h"

int main() {
  bigint_t *ac, *ad, *a1;

  big_init_m(3, &ac, &ad, &a1);
  big_alloc_max_m(3, &ac, &ad, &a1);

  // Sanity checks
  big_set("12231337221", &ac);
  big_set("21173313112", &ad);
  big_mul(ac, ad, &a1);
  big_assert("258977932758692941752", &a1);
  big_end_m(3, &ac, &ad, &a1);
  printf("OK\n");
}
```

