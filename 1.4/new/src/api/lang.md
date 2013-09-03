# lang 

> lang 是一套`underscore`风格的工具集，提供一些常用的工具函数，`lang` 模块内嵌在 `seed.js` 内，无需额外引入，这些函数直接挂载在 KISSY 全局对象上。

### augment()

`augment(r, s1 [, s2 , ...], ov = true, wl) => Function`

将 s1,s2.... 的 `prototype` 属性的成员复制到 `r.prototype` 上。这时被复制的成员来自于一个Fucntion对象，这个对象一般被称为掺元类（mixin class）。比如 KISSY 里的 CustemEvent 就是一个掺元类。掺元类只是被扩充用的。参数说明：

#### parameters

- r (function) – 将要扩充的函数
- `...s1` (function|object) – 扩充来源函数或对象. 非函数对象时复制的就是 s 的成员.
- ov (boolean) – 是否覆盖 r.prototype 同名属性.
- whitelist (Array<string>) – 属性来源对象的属性白名单, 仅在名单中的属性进行复制.

#### return

- `r`（function），即将要扩充的函数

#### Example

