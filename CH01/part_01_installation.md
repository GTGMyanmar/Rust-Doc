# Installation

## How to insall on linux

Linux မှာ install ဖို့အတွက် အောက်က command ကို terminal ထဲရိုက်ထည့်လိုက်ပါ။

```console
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

Command က script ကို download ပြီးတော့ `rustup` ကို install ပါလိမ့်မယ်။ installation က အဆင်ပြေတယ်ဆိုရင် ပြီးသွားတဲ့အခါ `Rust is installed now. Great!` ဆိုတဲ့စာသားကိုမြင်တွေ့ရမှာဖြစ်ပါတယ်။

Rust install တာအဆင်ပြေမပြေစစ်ဖို့အတွက် `rustup --versio`, `rustc --version` နဲ့ `cargo --version` ဆိုတဲ့ command တွေကို terminal ထဲရိုက်ထည့်လိုက်ကြည့်ပါ။ အောက်မှာပြထားတဲ့အတိုင်းတွေ့ရတယ်ဆိုအဆင်ပြေပါပြီ။

```console
(base) aung@aung:~$ rustup --version
rustup 1.22.1 (b01adbbc3 2020-07-08)
(base) aung@aung:~$ rustc --version
rustc 1.47.0 (18bf6b4f0 2020-10-07)
(base) aung@aung:~$ cargo --version
cargo 1.47.0 (f3c7e066a 2020-08-28)
```

* `rustup` ဆိုတာက rust version တွေနဲ့ toolchains တွေကို စီမံဖို့ အသုံးပြုရတဲ့ command line program တစ်ခုပဲဖြစ်ပါတယ်။ Rust ကို update လုပ်ဖို့ `rustup update` ဆိုတဲ့ command ကို အသုံးပြုနိုင်ပြီး `rustup self uninstall` command ကိုသုံးပြီးတော့လည်း Rust ကို uninstall နိုင်ပါတယ်။ `rustup doc` command သုံးပြီးတော့လည်း စက်ထဲမှာ install ထားတဲ့ documentation တွေကို offline အနေနဲ့ဖတ်နိင်ပါတယ်။

* `rustc` ဆိုတာကတော့ Rust compiler ဖြစ်ပြီး rust source ကို binary code အဖြစ် ပြောင်းပေးတဲ့ program ဖြစ်ပါတယ်။

* `cargo` ဆိုတာကတော့ project management လုပ်ပေးတဲ့ program တစ်ခုပါ။ prject create တာ လိုအပ်တဲ့ library တွေကို ရယူတာတွေနဲ့ တခြားအသုံးဝင်တဲ့ လုပ်ဆောင်ချက်တွေကိုလုပ်ပေးနိုင်ပါတယ်။

</br>

> Linux machine မှာ rust စစသုံးချင်း compile မရတာတွေဖြစ်တတ်ပါတယ်။ အဲလိုဖြစ်လာမယ်ဆိုရင် `gcc` နဲ့ `cmake` စစ်ကြည့်လိုက်ပါ မရှိရင် install ပေးလိုက်တာနဲ့ အဆင်ပြေသွားမှာဖြစ်ပါတယ်။

[the user forum](https://users.rust-lang.org/) နဲ့ [stack overflow](https://stackoverflow.com/questions/tagged/rust) နေရာတွေမှာလည်း လိုအပ်တာတွေကိုဝင်ရောက်ရှာဖွေနိင်ပါတယ်။

 [Rust programming language official page](https://www.rust-lang.org/tools/install) မှာပြထားတဲ့အတိုင်းလိုက်လုပ်ပြီးလည်း install နိုင်ပါတယ်။

Windows user တွေအနေနဲ့ [installနည်းကိုဒီမှာဝင်ကြည့်နိုင်ပါတယ်။](https://forge.rust-lang.org/infra/other-installation-methods.html)

<hr>

[prev. Introduction](https://github.com/GTGMyanmar/Rust-Doc/blob/main/Introduction/introduction.md)

[next. Hello, World!](https://github.com/GTGMyanmar/Rust-Doc/blob/main/CH01/part_02_hello.md)
