﻿<h4>AES-128 Block Cipher</h4>

<p>AES-dust is a compact Implementation of the AES-128 block cipher. There's support for Counter (CTR) and Electronic Codebook (ECB) modes of encryption.</p>

<p>The code is intentionally optimized for size rather than speed making it suitable for resource constrained environments.</p>

<h4>Side channel attacks</h4>

<p>AES was never intended to be resistant against side channel attacks. However, if you decide to use this code for an embedded project that requires a high level of security, first evaluate whether the code is sufficient against such attacks before using in your project.</p>

<h4>Files</h4>

<p>All files with .s and .asm extensions are compatible with the GNU assembler (GAS) except for the files in the MSVC folder that will assemble with either NASM or YASM.</p>

<table>
  <tr>
    <th>File</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>ax.asm</td>
    <td>x86 assembly</td>
  </tr>
  <tr>
    <td>axx.asm</td>
    <td>AMD64 assembly</td>
  </tr>
  <tr>
    <td>ax.s</td>
    <td>ARM32 assembly</td>
  </tr>
  <tr>
    <td>axx.s</td>
    <td>ARM64 assembly</td>
  </tr>
  <tr>
    <td>aes.c</td>
    <td>C source</td>
  </tr>
  <tr>
    <td>test.c</td>
    <td>Test unit with AES test vectors</td>
  </tr>
  <tr>
    <td>tweet.c</td>
    <td>Tweetable version of aes.c</td>
  </tr>
</table>

<h4>Assembly</h4>

<p>The below table shows code sizes for the hand written versions of AES-128</p>

<table>
  <tr>
    <th>Architecture</th>
    <th>ECB</th>
    <th>CTR</th>
  </tr>
  <tr>
    <td>x86</td>
    <td>205</td>
    <td>272</td>
  </tr>
  <tr>
    <td>AMD64</td>
    <td>253</td>
    <td>339</td>
  </tr>
  <tr>
    <td>ARM32</td>
    <td>376</td>
    <td></td>
  </tr>
  <tr>
    <td>ARM64</td>
    <td>388</td>
    <td></td>
  </tr>
</table>

<h4>C generated assembly</h4>

<p>The following table lists the size of assembly code generated by the GNU C compiler.</p>

<table>
  <tr>
    <th>Architecture</th>
    <th>ECB</th>
    <th>CTR</th>
  </tr>
  <tr>
    <td>x86</td>
    <td>538</td>
    <td>715</td>
  </tr>
  <tr>
    <td>AMD64</td>
    <td>481</td>
    <td>712</td>
  </tr>
  <tr>
    <td>ARM32</td>
    <td>480</td>
    <td>668</td>
  </tr>
  <tr>
    <td>ARM64</td>
    <td>640</td>
    <td>940</td>
  </tr>
</table>

<p>The following table lists the size of assembly code generated by the Microsoft C compiler.</p>

<table>
  <tr>
    <th>Architecture</th>
    <th>ECB</th>
    <th>CTR</th>
  </tr>
  <tr>
    <td>x86</td>
    <td>321</td>
    <td>477</td>
  </tr>
  <tr>
    <td>AMD64</td>
    <td>486</td>
    <td>673</td>
  </tr>
  <tr>
    <td>ARM32</td>
    <td>372</td>
    <td>502</td>
  </tr>
  <tr>
    <td>ARM64</td>
    <td>536</td>
    <td>880</td>
  </tr>
</table>

<h4>Licensing information</h4>

<p>Initially this was published with a BSD license. I decided to unlicense hoping more people would use and provide useful feedback.</p>

<pre>
This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>
</pre>
