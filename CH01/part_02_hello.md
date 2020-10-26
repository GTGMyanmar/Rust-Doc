# Hello, World

Rust ကို install ပြီးပြီဆိုတော့ programming language တွေရဲ့ထုံးစံအတိုင်း `hello_world` ဆိုတဲ့ program လေးနဲ့စလိုက်ရအောင်။

ကြိုက်တဲ့ directory တစ်ခုမှာ hello_world.rs ဆိုတဲ့ file တစ်ခုကို အသစ်လုပ်လိုက်ပါ။ linux machine တွေမှာဆို `touch hello_world.rs` ရိုက်ထည့်ပြီးလက်ရှိ directory မှာ file create လို့ရပါတယ်။ အဲဒီ file ကိုဖွင့်ပြီး အောက်က code ကိုစာလုံးအတိအကျရေးထည့်ပြီး save လိုက်ပါ။

```Rust
fn main() {
    println!("Hello, World!");
}
```

`fn` ဆိုတာက function ကို declare တဲ့ keyword ပဲဖြစ်ပါတယ်။ Executable file ကိုဆောက်ဖို့ဆိုရင် `main` function မဖြစ်မနေထည့်ပေးရမှာပါ။ Executable code တွေမှာ `main` အပိုင်းကိုအရင်ဆုံး run ပါတယ်။ `main` အနောက်က `()` ကွင်းလေးက function argument ထည့်တဲ့နေရာပါ။ `main` function မှာတော့ ဘာ argument မှမလိုပါဘူး။ Function အကြောင်းအသေးစိတ်ကို function ရှင်းပြတဲ့အခန်းမှာမှ ဆက်ပြောပြပါမယ်။

`println!` ဆိုတာက print line ကို ဆိုလိုတာဖြစ်ပါတယ်။ terminal ကနေတစ်ဆင့် output ကိုဖော်ပြပေးဖို့သုံးတာပါ။ အနောက်မှာ `!`လေးပါတာကိုသတိထားမိမယ်ထင်ပါတယ်။ Rust မှာ အဲလို code မျိုးကို `marcro` လို့ခေါ်ပါတယ်။ function တွေနဲ့ဆင်တူပေမဲ့ function မဟုတ်ပါဘူး။ အဲကွင်းထဲမှာ ရှိတဲ့ `Hello, World!` ဆိုတဲ့စာကို terminal မှာပြန်ထုတ်ပေးမှာဖြစ်ပါတယ်။ C/C++ မှာလို `\n` ဆိုတဲ့ new line character ထည့်စရာမလိုပါဘူး။ `println!` macro က အပြီးထည့်ထားပေးလို့ပဲဖြစ်ပါတယ်။ ဒီ code မှာနောက်ဆုံးက semicolon လေးက မပါလည်း အလုပ်လုပ်မှာဖြစ်ပေမဲ့ထည့်ဖို့မမေ့ပါနဲ့။ ဘာကြောင့်လဲဆိုတာ function တွေကိုရှင်းပြတဲ့အခန်းမှာမှထည့်ရှင်းပြပါမယ်။

</br>

## Compile with `rustc` command

အရှေ့မှာပြောခဲ့သလိုပဲ `rustc` က rust ရဲ့ compiler ပါ။ အရင်ဆုံး အဲတာကိုသုံးပြီး compile ကြည့်ကြရအောင်။ Terminal မှာ `rustc hello_world.rs` ဆိုပြီးရိုက်ထည့်လိုက်ပါ။ `hello_world` ဆိုတဲ့ file အသစ်လေးပေါ်လာမှာဖြစ်ပါတယ်။ အဲဒီ file လေးက ကျွန်တော်တို့လိုချင်တဲ့ binary executable file ပဲဖြစ်ပါတယ်။ `./hello_world` လို့ရိုက်ထည့်ပြီး run ကြည့်ပါက `Hello, World!` ဆိုတဲ့စာသားပေါ်လာတာကိုမြင်ရမှာဖြစ်ပါတယ်။ Congratulation ပါ သင် hello_world program ကို အောင်မြင်စွာရေးလိုက်နိုင်ပြီဖြစ်ပါတယ်။ အဲဒီ binary file ကို ကူးပြီးတော့ linux machine တွေမှာ run လို့ရပါပြီ။

hello_world program လိုမျိုးတွေကတော့ `rustc` နဲ့ compile ရတာအဆင်ပြေပေမဲ့ project ကြီးတွေမှာလိုမျိုး library တွေကိုသုံးရတာတို့ file အများကြီးနဲ့ရေးရတဲ့အခါတွေမှာ တအားအဆင်မပြေဖြစ်တတ်ပါတယ်။ အဲအတွက် Rust team က cargo ဆိုတဲ့ project management tool တစ်ခုလုပ်ထားပေးပါတယ်။ အဲတာလေးကိုသုံးကြည့်ရအောင်။

</br>

## Crate Project with `cargo` Command

`cargo` ကို Rust install လိုက်ကတည်းက ထည့်ပေးထားတာပဲဖြစ်ပါတယ်။ `cargo new hello-world` ဆိုတဲ့ command ကို run လိုက်ရင် အောက်ကပြထားတဲ့အတိုင်းထွက်လာတာကိုတွေ့ရပါလိမ့်မယ်။

```console
 aung@aung:~/col/rust/Project$ cargo new hello-world --bin
     Created binary (application) `hello-world` package
```

Rust project မှာ _binary_ နဲ့ _library_ ဆိုပြီး နှစ်မျိုးရှိပါတယ်။ `binary` ဆိုတာက executable program တည်ဆောက်ဖို့အတွက်သုံးတာဖြစ်ပါတယ်။ cargo command ရဲ့ default က binary crate ကိုဆောက်တာဖြစ်တာကြောင့် `cargo new hello-world` တည်းနဲ့လည်းဆောက်လို့ရပါတယ်။ Library crate ကိုဆောက်ချင်ရင်တော့ `cargo new hello-world --lib` ဆိုပြီးတော့ဆောက်ရမှာပါ။ အောက်က terminal output ကိုကြည့်ကြည့်ပါ။

```console
aung@aung:~$ cargo new hello-world --lib
     Created library `hello-world` package
```

Operating system တိုင်းအတွက် cargo command တွေက အတူတူဖြစ်တာကြောင့် အသုံးပြုရတာပိုအဆင်ပြေစေမှာဖြစ်ပါတယ်။

cargo နဲ့ဆောက်လိုက်တဲ့ project တွေမှာ git ကိုပါတစ်ခါတည်း initialized ပေးထားမှာဖြစ်ပါတယ်။ Git ကို အစပြုထားပြီးသား directory တွေမှာ project ဆောက်ရင်တော့ git ကို မစထားပေးပဲ ကျော်လိုက်မှာပါ။ `cargo new --vcs=git` ဆိုတဲ့ command ကိုသုံးပြီးတော့ git ကို manually initialize နိုင်ပါတယ်။ `cargo new` command ရဲ့တခြား လုပ်ဆောင်ချက်တွေကို `cargo new --help` command သုံးပြီးတော့လည်းစစ်ကြည့်နိုင်ပါတယ်။

</br>

## Structure of the Crate

Cargo နဲ့ create လိုက်တဲ့ crate ရဲ့ တည်ဆောက်ပုံကို လေ့လာကြည့်ရအောင်။ အောက်က terminal output ကိုကြည့်ကြည့်ပါ။

```console
aung@aung:~/col/rust/Project/test$ tree hello-world/
hello-world/
├── Cargo.toml
└── src
    └── main.rs

1 directory, 2 files
```

`hello-world` ဆိုတဲ့ project directory ထဲမှာ `Cargo.toml` ဆိုတဲ့ configuration file နဲ့ `src` directory ကိုတွေ့ရမှာပါ။ `src` ထဲမှာဆိုရင် `main.rs` ဆိုတဲ့ file ကိုတွေ့ရမှာဖြစ်ပါတယ်။ project directory က binary crate ဖြစ်တာကြောင့် `main.rs` ကို _root file_ အနေသတ်မှတ်ပါတယ်။ Library crate မှာဆိုရင် root file အနေနဲ့ `lib.rs` ကိုတွေ့ရမှာပါ။

`Cargo.toml` file ကိုဖွင့်ကြည့်လိုက်ရင်အောက်မှာပြထားတဲ့အတိုင်းတွေ့ရမှာဖြစ်ပါတယ်။

```toml
[package]
name = "hello-world"
version = "0.1.0"
authors = ["your_name <youraddress@example.com>"]
edition = "2018"

# See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html

[dependencies]

```

`[package]` ဆိုတဲ့ ့heading အောက်ကိုက `name` ဆိုတာကတော့ သင့် project directory ရဲ့ name ဖြစ်ပါတယ်။ `version` ကတော့ လက်ရှိ project ရဲ့ version ပဲဖြစ်ပါတယ်။ `author` နေရာမှာတော့ သင့်ရဲ့ local machine မှာသိမ်းထားတဲ့ information ကိုယူပြီး ဖြည့်ထားပေးမှပါ၊ တကယ်လို့ သိမ်းထားတဲ့ information မရှိဘူးဆိုရင် ကိုယ်တိုင်ပြင်ရမှာဖြစ်ပါတယ်။ `edition` ကတော့ Rust ရဲ့ edition အသစ်ထွက်တဲ့ ခုနှစ်ဖြစ်တဲ့ `2018`လို့ပြထားမှာဖြစ်ပါတယ်။

`[dependencies]` အောက်မှာကတော့ ကိုယ့် project မှာလိုအပ်တဲ့ crate တွေကို version နဲ့ တွဲဖြည့်ပေးရမှာပါ၊ compile တဲ့ အခါကျရင် Cargo က crates.io မှာရှိနေတဲ့ လိုအပ်တဲ့ crate တွေကို auto download ပြီး compile ပေးမှာပါ။

`src/main.rs` ကိုဖွင့်ကြည့်လိုက်မယ်ဆိုရင်အောက်ကအတိုင်းတွေ့ရမှာပါ။

```Rust
fn main() {
    println!("Hello, world!");
}
```

Rust က `hello-world` program ကို auto generate ပေးထားမှာပဲဖြစ်ပါတယ်။ ရေးချင်တဲ့ program ကို အဲမှာပြင်ရေးလို့ရပါပြီ။

</br>

## Building and Running Project with `cargo` command

ဒါဆို cargo ကိုသုံးပြီး `hello-world` program ကို တည်ဆောက်ကြည့်ရအောင်။

```console
(base) aung@aung:~/col/rust/Rust-Doc/code/hello-world$ cargo build
   Compiling hello-world v0.1.0 (/home/aung/col/rust/Rust-Doc/code/hello-world)
    Finished dev [unoptimized + debuginfo] target(s) in 1.81s
```

`cargo build` command က executable file ကို `target/debug/hello-world` ဆိုတဲ့နေရာမှာ create ပေးမှာဖြစ်ပါတယ်၊ အောက်မှာပြထားတဲ့အတိုင်း run ကြည့်နိုင်ပါတယ်။

```console
(base) aung@aung:~/col/rust/Rust-Doc/code/hello-world$ ./target/debug/hello-world
Hello, world!
```

`cargo build` ဆိုတဲ့ command ကို run လိုက်တာနဲ့ project directory မှာ `Cargo.lock` ဆိုတဲ့ file တစ်ခုပိုလာတာကိုတွေ့ရမှာဖြစ်ပါတယ်။ အဲဒီ file မှာ prject အတွက်လိုအပ်တဲ့ dependencies တွေကို version နဲ့ အတိအကျ သိမ်းထားမှာဖြစ်ပါတယ်။ သင့်အနေနဲ့ အဲဒီ file ကိုပြင်စရာမလိုပါဘူး။ Cargo ကအလိုလျောက်ပြင်ပေးမှာပဲဖြစ်ပါတယ်။

`cargo build` နဲ့ compile ပြီး သီးသန့်တစ်ခေါက်ပြန် run ရတာ အကြိမ်များလာရင်တကယ်စိတ်ရှုပ်စရာကောင်းပါတယ်။ ဒါကြောင့် cargo မှာ `cargo run` ဆိုတဲ့ command ရှိပါတယ်။ ဒီ command ကိုရိုက်ထည့်လိုက်တာနဲ့ compile ပြီးတစ်ခါတည်း output ကိုထုတ်ပေးတာကို အောက်ကအတိုင်းမြင်ရမှာပဲဖြစ်ပါတယ်။

```console
(base) aung@aung:~/col/rust/Rust-Doc/code/hello-world$ cargo run
    Finished dev [unoptimized + debuginfo] target(s) in 0.04s
     Running `target/debug/hello-world`
Hello, world!
```

`cargo check` command နဲ့လည်း ကိုယ်ရေးထားတဲ့ code က error မတက်ဘဲ compile ရမရစစ်ဆေးနိုင်မှာဖြစ်ပါတယ်။ `cargo build` နဲ့ `cargo check` ရဲ့ကွာခြားချက်က `cargo check` command က executable file ကိုဆောက်ပေးတဲ့လုပ်ဆောင်ချက်ကိုကျော်လိုက်တာကြောင့် အများကြီးပိုမြန်မှာဖြစ်ပါတယ်။

```console
(base) aung@aung:~/col/rust/Rust-Doc/code/hello-world$ cargo check
    Checking hello-world v0.1.0 (/home/aung/col/rust/Rust-Doc/code/hello-world)
    Finished dev [unoptimized + debuginfo] target(s) in 0.12s
```

</br>

## Development and Release Profile

`cargo build` ရဲ့ output ကိုကြည့်ကြည့်ရအောင်။

```console
(base) aung@aung:~/col/rust/Rust-Doc/code/hello-world$ cargo build
   Compiling hello-world v0.1.0 (/home/aung/col/rust/Rust-Doc/code/hello-world)
    Finished dev [unoptimized + debuginfo] target(s) in 1.81s
```

နောက်ဆုံးအကြောင်းမှာ `Finished dev [unoptimized + debuginfo]` ဆိုတာကိုတွေ့ရပါလိမ့်မယ်။ Cargo မှာ _developement_ နဲ့ _release_ ဆိုတဲ့ profile နှစ်ခုရှိပါတယ်။ Development profile မှာက compilation speed မြန််ဖို့အတွက် optimization တွေကိုလျော့ချထားပါတယ်။ တကယ်လို့သင်သာသင့် project ကိုလက်တွေ့အသုံးချဖို့အတွက် compile မယ်ဆို `cargo build --release` ဆိုပြီး compile သင့်ပါတယ်။ ဒီ command ကသင့် project performance အတွက် လိုအပ်တဲ့ optimization တွေကိုအလိုလျောက်ထည့်ပေါင်းပေးမှာဖြစ်ပါတယ်။

Github ပေါ်က rust projectတွေလည်းကို clone ပြီး cargo command သုံး၍ compile ပြီးတော့ အသုံးပြုနိုင်ပါသေးတယ်။

ဆက်လက်ပြီးတော့ programming အခြေခံသဘောတရားများနှင့် Rust ရဲ့ basic data types တွေကိုလေ့လာကြရအောင်။

<hr>

[prev. Installation](./part_01_installation.md)

[next. Programming အခြေခံသဘောတရားများ](../CH02/Programmingအခြေခံသဘောတရားများ.md)
