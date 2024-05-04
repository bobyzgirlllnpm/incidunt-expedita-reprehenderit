# @bobyzgirlllnpm/incidunt-expedita-reprehenderit
---

[![Build Status](https://travis-ci.org/aligay/@bobyzgirlllnpm/incidunt-expedita-reprehenderit.svg?branch=master)](https://travis-ci.org/aligay/@bobyzgirlllnpm/incidunt-expedita-reprehenderit/branches)
[![codecov](https://codecov.io/gh/aligay/@bobyzgirlllnpm/incidunt-expedita-reprehenderit/branch/master/graph/badge.svg)](https://codecov.io/gh/aligay/@bobyzgirlllnpm/incidunt-expedita-reprehenderit)
[![dependencies Status](https://david-dm.org/aligay/@bobyzgirlllnpm/incidunt-expedita-reprehenderit/status.svg)](https://david-dm.org/aligay/@bobyzgirlllnpm/incidunt-expedita-reprehenderit)
[![devDependencies Status](https://david-dm.org/aligay/@bobyzgirlllnpm/incidunt-expedita-reprehenderit/dev-status.svg)](https://david-dm.org/aligay/@bobyzgirlllnpm/incidunt-expedita-reprehenderit?type=dev)

## install
```
npm install @bobyzgirlllnpm/incidunt-expedita-reprehenderit
```
## use
```
import safeTrim from '@bobyzgirlllnpm/incidunt-expedita-reprehenderit'
safeTrim('    a      b  ')
```

## remove Invisible spaces

```
let str = '  "a":1    a \r\n\r\t  ᠎             　b       '
let ret = safeTrim(str)
expect(ret).toEqual('"a":1    a\n\nb')
```

## convert CR CR-LR into LR
```
a\r\n\r\nb  => 'a\n\nb'
a\r\rb => 'a\n\nb'
a\r\r\nb => 'a\n\nb'
```

## remove BOM
```
JSON.parse('﻿{"a":1}') // ❗️Error because BOM

JSON.parse(safeTrim('﻿{"a":1}')) // ✅
```


## more feature
[more feature](spec/test_spec.js)
