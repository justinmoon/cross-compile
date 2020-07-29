# Setup

- `apt install mingw-w64`
- `rustup target add i686-pc-windows-gnu`
`rustup target add x86_64-pc-windows-gnu`
- Add the following to your [cargo config](https://doc.rust-lang.org/cargo/reference/config.html#hierarchical-structure):
```
[target.x86_64-pc-windows-gnu]
linker = "/usr/bin/x86_64-w64-mingw32-gcc"

[target.i686-pc-windows-gnu]
linker = "i686-w64-mingw32-gcc"
```

# Run

## x86_64

```
$ cargo build --target x86_64-pc-windows-gnu
warning: Both `/home/justin/.cargo/config` and `/home/justin/.cargo/config.toml` exist. Using `/home/justin/.cargo/config`
    Finished dev [unoptimized + debuginfo] target(s) in 0.23s
```

# i686

```
$ cargo build --target i686-pc-windows-gnu
warning: Both `/home/justin/.cargo/config` and `/home/justin/.cargo/config.toml` exist. Using `/home/justin/.cargo/config`
   Compiling ccwin v0.1.0 (/mnt/c/Users/justin/dev/ccwin)
error: linking with `i686-w64-mingw32-gcc` failed: exit code: 1
  |
  = note: "i686-w64-mingw32-gcc" "-fno-use-linker-plugin" "-Wl,--nxcompat" "-nostdlib" "-Wl,--large-address-aware" "/usr/i686-w64-mingw32/lib/crt2.o" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/rsbegin.o" "-L" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib" "/mnt/c/Users/justin/dev/ccwin/target/i686-pc-windows-gnu/debug/deps/ccwin-6fbb34f57baba4cb.1noh9502nlslw6xv.rcgu.o" "/mnt/c/Users/justin/dev/ccwin/target/i686-pc-windows-gnu/debug/deps/ccwin-6fbb34f57baba4cb.1sibhsb3j3hr3kjf.rcgu.o" "/mnt/c/Users/justin/dev/ccwin/target/i686-pc-windows-gnu/debug/deps/ccwin-6fbb34f57baba4cb.2bjcww6brosqhe8a.rcgu.o" "/mnt/c/Users/justin/dev/ccwin/target/i686-pc-windows-gnu/debug/deps/ccwin-6fbb34f57baba4cb.2l2l5bbvp5ujanm0.rcgu.o" "/mnt/c/Users/justin/dev/ccwin/target/i686-pc-windows-gnu/debug/deps/ccwin-6fbb34f57baba4cb.2r6463zjcjatf4gc.rcgu.o" "/mnt/c/Users/justin/dev/ccwin/target/i686-pc-windows-gnu/debug/deps/ccwin-6fbb34f57baba4cb.yue2646euox1qaw.rcgu.o" "-o" "/mnt/c/Users/justin/dev/ccwin/target/i686-pc-windows-gnu/debug/deps/ccwin-6fbb34f57baba4cb.exe" "/mnt/c/Users/justin/dev/ccwin/target/i686-pc-windows-gnu/debug/deps/ccwin-6fbb34f57baba4cb.1vb46amjohv93n30.rcgu.o" "-Wl,--gc-sections" "-nodefaultlibs" "-L" "/mnt/c/Users/justin/dev/ccwin/target/i686-pc-windows-gnu/debug/deps" "-L" "/mnt/c/Users/justin/dev/ccwin/target/debug/deps" "-L" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib" "-Wl,--start-group" "-Wl,-Bstatic" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libstd-d4d98dbb25b105db.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libpanic_unwind-aea8e86c045f6ac9.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libhashbrown-fe93d9ee775887a6.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/librustc_std_workspace_alloc-feec135147f84ace.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libbacktrace-df89298572d659bc.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libbacktrace_sys-d061a1023aebf70d.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/librustc_demangle-a47adadafd80ac4b.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libunwind-4faa837b00fc5bfd.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libcfg_if-1e1407ff59f903a0.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/liblibc-19653faa8ec1baa3.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/liballoc-19b9a6efee72d3d1.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/librustc_std_workspace_core-7eb0ac6ed41679d7.rlib" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libcore-9c5ebf9e94129f57.rlib" "-Wl,--end-group" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libcompiler_builtins-312f72119557f352.rlib" "-Wl,-Bdynamic" "-ladvapi32" "-lws2_32" "-luserenv" "-lmingwex" "-lmingw32" "-lmsvcrt" "-lmsvcrt" "-luser32" "-lkernel32" "-lgcc_eh" "-l:libpthread.a" "-lgcc" "-lmsvcrt" "-lkernel32" "/home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/rsend.o"
  = note: /usr/bin/i686-w64-mingw32-ld: /mnt/c/Users/justin/dev/ccwin/target/i686-pc-windows-gnu/debug/deps/ccwin-6fbb34f57baba4cb.2l2l5bbvp5ujanm0.rcgu.o: in function `ZN4core3ops8function6FnOnce9call_once17h251fb3ccc9676465E':
          /rustc/49cae55760da0a43428eba73abcb659bb70cf2e4\src\libcore\ops\function.rs:232: undefined reference to `_Unwind_Resume'
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libstd-d4d98dbb25b105db.rlib(std-d4d98dbb25b105db.std.f5jmee2i-cgu.0.rcgu.o): in function `ZN64_$LT$std..backtrace..BytesOrWide$u20$as$u20$core..fmt..Debug$GT$3fmt17h26758117dc811c22E':
          /rustc/49cae55760da0a43428eba73abcb659bb70cf2e4\/src\libstd/backtrace.rs:229: undefined reference to `_Unwind_Resume'
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libstd-d4d98dbb25b105db.rlib(std-d4d98dbb25b105db.std.f5jmee2i-cgu.0.rcgu.o): in function `ZN4core3ops8function6FnOnce9call_once17h6cef60404fcca0f6E':
          /rustc/49cae55760da0a43428eba73abcb659bb70cf2e4\src\libcore\ops/function.rs:232: undefined reference to `_Unwind_Resume'
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libstd-d4d98dbb25b105db.rlib(std-d4d98dbb25b105db.std.f5jmee2i-cgu.0.rcgu.o): in function `ZN4core3ops8function6FnOnce9call_once17hffda90729e2269daE':
          /rustc/49cae55760da0a43428eba73abcb659bb70cf2e4\src\libcore\ops/function.rs:232: undefined reference to `_Unwind_Resume'
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libstd-d4d98dbb25b105db.rlib(std-d4d98dbb25b105db.std.f5jmee2i-cgu.0.rcgu.o): in function `ZN4core3ptr13drop_in_place17ha996cfbc1bafe8e3E':
          /rustc/49cae55760da0a43428eba73abcb659bb70cf2e4\src\libcore\ptr/mod.rs:177: undefined reference to `_Unwind_Resume'
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libstd-d4d98dbb25b105db.rlib(std-d4d98dbb25b105db.std.f5jmee2i-cgu.0.rcgu.o):/rustc/49cae55760da0a43428eba73abcb659bb70cf2e4\src\libcore\ptr/mod.rs:177: more undefined references to `_Unwind_Resume' follow
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libpanic_unwind-aea8e86c045f6ac9.rlib(panic_unwind-aea8e86c045f6ac9.panic_unwind.1rrga019-cgu.0.rcgu.o): in function `ZN12panic_unwind8real_imp5panic17h2fbb325cd5bbabebE':
          /rustc/49cae55760da0a43428eba73abcb659bb70cf2e4\/src\libpanic_unwind/gcc.rs:62: undefined reference to `_Unwind_RaiseException'
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libbacktrace-df89298572d659bc.rlib(backtrace-df89298572d659bc.backtrace.63laijh3-cgu.0.rcgu.o): in function `ZN9backtrace7dbghelp4init17h76808fe8072f6946E':
          C:\Users\VssAdministrator\.cargo\registry\src\github.com-1ecc6299db9ec823\backtrace-0.3.46/C:\Users\VssAdministrator\.cargo\registry\src\github.com-1ecc6299db9ec823\backtrace-0.3.46\src/dbghelp.rs:360: undefined reference to `_Unwind_Resume'
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libbacktrace-df89298572d659bc.rlib(backtrace-df89298572d659bc.backtrace.63laijh3-cgu.0.rcgu.o): in function `ZN9backtrace9symbolize12libbacktrace10syminfo_cb17hc5f0b6446d3ace38E':
          C:\Users\VssAdministrator\.cargo\registry\src\github.com-1ecc6299db9ec823\backtrace-0.3.46/C:\Users\VssAdministrator\.cargo\registry\src\github.com-1ecc6299db9ec823\backtrace-0.3.46\src\symbolize/libbacktrace.rs:210: undefined reference to `_Unwind_Resume'
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/libbacktrace-df89298572d659bc.rlib(backtrace-df89298572d659bc.backtrace.63laijh3-cgu.0.rcgu.o): in function `ZN9backtrace9symbolize12libbacktrace9pcinfo_cb17h35e0ab49ed658137E':
          C:\Users\VssAdministrator\.cargo\registry\src\github.com-1ecc6299db9ec823\backtrace-0.3.46/C:\Users\VssAdministrator\.cargo\registry\src\github.com-1ecc6299db9ec823\backtrace-0.3.46\src\symbolize/libbacktrace.rs:244: undefined reference to `_Unwind_Resume'
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/liballoc-19b9a6efee72d3d1.rlib(alloc-19b9a6efee72d3d1.alloc.9g3thvjy-cgu.0.rcgu.o): in function `ZN92_$LT$alloc..borrow..Cow$LT$str$GT$$u20$as$u20$core..ops..arith..AddAssign$LT$$RF$str$GT$$GT$10add_assign17hfdefff7d026801b9E':
          /rustc/49cae55760da0a43428eba73abcb659bb70cf2e4\/src\liballoc/borrow.rs:456: undefined reference to `_Unwind_Resume'
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/liballoc-19b9a6efee72d3d1.rlib(alloc-19b9a6efee72d3d1.alloc.9g3thvjy-cgu.0.rcgu.o): in function `ZN77_$LT$alloc..borrow..Cow$LT$str$GT$$u20$as$u20$core..ops..arith..AddAssign$GT$10add_assign17h5a0d5e7136a19909E':
          /rustc/49cae55760da0a43428eba73abcb659bb70cf2e4\/src\liballoc/borrow.rs:475: undefined reference to `_Unwind_Resume'
          /usr/bin/i686-w64-mingw32-ld: /home/justin/.rustup/toolchains/stable-x86_64-unknown-linux-gnu/lib/rustlib/i686-pc-windows-gnu/lib/liballoc-19b9a6efee72d3d1.rlib(alloc-19b9a6efee72d3d1.alloc.9g3thvjy-cgu.0.rcgu.o):/rustc/49cae55760da0a43428eba73abcb659bb70cf2e4\/src\liballoc/fmt.rs:588: more undefined references to `_Unwind_Resume' follow
          /usr/bin/i686-w64-mingw32-ld: /usr/lib/gcc/i686-w64-mingw32/9.3-win32/libgcc_eh.a(unwind-sjlj.o):(.text+0xdf): undefined reference to `__mingwthr_key_dtor'
          collect2: error: ld returned 1 exit status
          

error: aborting due to previous error

error: could not compile `ccwin`.

To learn more, run the command again with --verbose.

```