# Programming အခြေခံသဘောတရားများ

ဒီတစ်ခါမှာတော့ တစ်ခြား programming language တွေမှာ တွေ့မြင်နေကျဖြစ်တဲ့ မဖြစ်မနေသိထားရမဲ့ variable declaration တွေ basic data types, function တွေကိုတည်ဆောက်ပုံတွေနဲ့ control flow တွေကိုဘယ်လိုလုပ်ရလဲစတာတွေကိုလေ့လာရမှာဖြစ်ပါတယ်။

> Variables တွေကိုဘယ်လို declare ရလဲ မပြောခင်မှာ _keyword_ တွေအကြာင်းကိုအရင်လေ့လာကြည့်ရအောင်။ Keywords တွေဆိုတာက programming language တစ်ခုစီမှာ နဂိုကတည်းက လုပ်ဆောင်ချက်တွေကိုသတ်မှတ်ထားပြီးသားဖြစ်တဲ့ စာလုံးတွေဖြစ်ပါတယ်။ ၄င်း keywords တွေကို ကျွန်တော်တို့ variables တို့ function name တို့အဖြစ် declare လို့ရမှာမဟုတ်ပါဘူး။

</br>

## Variables Declaration

Variable တွေကို ဘယ်လိုကြေညာရလဲမပြောခင်မှာ variable တွေဆိုတာဘာလဲ ဘယ်လိုအလုပ်လုပ်လဲဆိုတာအရင်ကြည့်ရအောင်။

variable သဘောတရားဆိုတာကျွန်တော်တို့နဲ့ရင်းနှီးနေကျဖြစ်ပါတယ်။ မှတ်ပုံတင်တို့မှာ `နာမည်: ဘယ်သူဘယ်ဝါ, အဖအမည်: ဘယ်သူဘယ်ဝါ` ဆိုတာမျိုးတွေရမှာပါ စာရင်းစစ်တဲ့သူက နာမည်သိချင်ရင် အများကြီးမေးစရာမလိုပါဘူး သူက `နာမည်` လို့ပြောလိုက်တာနဲ့ ကိုယ့်နာမည်ကို မေးမှန်းသိကြပါတယ်။ ဒီသဘောတရားမှာ `နာမည်` ဆိုတာသည် `variable` ကိုကိုယ်စားပြုတာဖြစ်ပါတယ်။

ဒါဆို variable ဆိုတာဘာလဲသဘောပေါက်လောက်ပြီမို့အောက်က code မှာ variable ဘယ်လို declare လဲကြည့်ကြရအောင်။

```Rust
fn main() {
    let x = 5;
}
```

Rust မှာ variable ကို ကြေညာဖို့အတွက် `let` ဆိုတဲ့ keyword ကိုသုံးရပါတယ်။ `=` ကိုတော့ asignment operator လို့ခေါ်ပါတယ်။ အဲဒီ code ရဲ့ အဓိပ္ပါယ်ကတော့ `x တန်ဖိုး 5 ဖြစ်ပါစေ` လို့ဖော်ပြပါတယ်။ code ရဲ့အဆုံးက `;` လေးကိုထည့်ဖို့မမေ့နဲ့ဦးနော်။

အောက်က code လေးကိုထပ်ကြည့်လိုက်ရအောင်။

```Rust
fn main() {
    let x = 5;
    println!("The value of x is: {}", x);
    x = 6;
    println!("The value of x is: {}", x);
}
```

run လိုက်ရင် အောက်ကအတိုင်း error ထွက်လာမှာကိုမြင်ရမှာဖြစ်ပါတယ်။

```console
(base) aung@aung:~/col/rust/project/Code/variables$ cargo run
   Compiling variables v0.1.0 (/home/aung/col/rust/project/Code/variables)
error[E0384]: cannot assign twice to immutable variable `x`
 --> src/main.rs:4:5
  |
2 |     let x = 5;
  |         -
  |         |
  |         first assignment to `x`
  |         help: make this binding mutable: `mut x`
3 |     println!("The value of x is: {}", x);
4 |     x = 6;
  |     ^^^^^ cannot assign twice to immutable variable

error: aborting due to previous error

For more information about this error, try `rustc --explain E0384`.
error: could not compile `variables`.

To learn more, run the command again with --verbose.
```

ဘာကြောင့် error တက်လဲဆိုတာအဖြေရှာကြည့်ရအောင်။ console output ထဲမှာ `cannot assign twice to immutable variable` ဆိုတဲ့ စာကိုတွေ့ရမှာဖြစ်ပါတယ်။ Rust မှာ immutable နဲ့ mutable variable နှစ်မျိုးပါတယ်။ immutable variable ဆိုတာကတော့ variable ကို declare ပြီးရင် တန်ဖိုးပြန်ပြောင်းလို့မရပါဘူး။ တကယ်လို့တန်ဖိုးကိုပြန်ပြောင်းချင်ရင် mutable variable ဖြစ်ရပါမယ်။ Rust မှာဘာကြောင့် ဒီ rule ကိုသုံးလဲဆိုရင် multi-thread program တွေမှာ တန်ဖိုးတွေ ကိုယ်သတိမထားမိဘဲ မတော်တဆပြောင်းပြီး bug တွေဖြစ်လာခြင်းမှကာကွက်ဖိုဖြစ်ပါတယ်။ variable ကို mutable အဖြစ်ကြေညာဖို့ဆိုရင် `mut` keyword ကိုသုံးရမှာဖြစ်ပါတယ်။ အောက်က code ကိုကြည့်ကြည့်ပါ။

```Rust
fn main() {
    let mut x = 5;
    println!("The value of x is: {}", x);
    x = 6;
    println!("The value of x is: {}", x);
}
```

ဒီ code ကို run ရင် အောက်ကအတိုင်းထွက်လာပါလိမ့်မယ်။ 

```console
$ cargo run
   Compiling variables v0.1.0 (file:///projects/variables)
    Finished dev [unoptimized + debuginfo] target(s) in 0.30s
     Running `target/debug/variables`
The value of x is: 5
The value of x is: 6
```

## Constant

တခြား programming language တွေမှာဆိုရင် _immutable variable_ ဆိုတာနဲ့ constant တွေကိုမြင်မိပါလိမ့်မယ်။ Rust မှာတော့ constant ဆိုတဲ့ type က သီးသန့်ရှိပါတယ်။ constant နဲ့ immutable variable တွေရဲ့ကွာခြားချက်ကတော့ Constant တွေမှာ `mut` keyword ကိုသုံးလို့မရပါဘူး။ Rust မှာ Constant variable တွေက အမြဲ immutable ဖြစ်ပါတယ်။

Constant တွေကိုကြေညာဖို့ `let` အစား `const` ဆိုတဲ့ keyword ကိုသုံးရမှာဖြစ်ပါတယ်။ const variable ရဲ့ type ဖော်ပြချက်ကိုလည်းမဖြစ်မနေထည့်ပေးရပါမယ်။ Constant Variable ကိုတော့ စာလုံးအကြီးတွေနဲ့ပဲဖော်ပြကြပါတယ်။ Constant Variable တွေကို function တွေရဲ့အပြင်ဘက်ဖြစ်တဲ့ global scope မှာပါကြေညာနိုင်ပါတယ်။ သတိထားရမှာက constant variables တွေရဲ့ တန်ဖိုးကို တိုက်ရိုက် _hardcoded_ ထည့်ရမှာဖြစ်ပါတယ် function တို့ method တို့ကနေပြန်ထုတ်ပေးတဲ့တန်ဖိုးမဖြစ်ရပါဘူး။

```Rust
const SPEED_OF_LIGHT: u32 = 300_000_000;
fn main() {
    println!("{}", SPEED_OF_LIGHT);
}
```

## Shadowing

```Rust
fn main() {
  let x = 5;
  let x = x + 5;

  println!("x: {}", x);
```

Variable ကိုကြေညာတဲ့ နေရာမှာ `mut` ကိုမသုံးဘဲ ဒီလိုမျိုး declare ကြည့်ကြလိမ့်မယ်လို့ထင်ပါတယ်။ ဒီ variable မျိုးကို _shadowing_ လို့ခေါ်ပါတယ်။ ရှိပြီးသား `x` ကိုမှထပ်ပြီးတော့ တစ်ဆင့် declare လိုက်တာပါ။ ကွာခြားချက်ကိုသိရဖို့အတွက်အောက်က code ကိုအရင်ကြည့်ကြည့်လိုက်ပါ။

```Rust
fn main() {
  let mut x = 5;
  x = 5.2;
}
```

ဒီ code မျိုးဆို error တက်ပါလိမ့်မယ်။ ဘာလို့လဲဆိုတော့ integer ဖြစ်တဲ့ `x` ထဲက တန်ဖိုး `5`ကိုထုတ်ပြီးတော့ floating point `5.2` ထည့်လိုက်လို့ပါ။

```Rust
fn main() {
  let x = 5;
  let x = 5.2;
}
```

ဒီလိုမျိုးကိုတော့ Rust က compile ပေးပါလိမ့်မယ်။ ဘာကြောင့်လဲဆိုတော့ integer type variable ဖြစ်တဲ့ `x` ကို နာမည်တူတဲ့ floating point type variable ဖြစ်တဲ့ `x`နဲ့ _shadow_ လိုက်လို့ပါ။ 

Variable တွေအကြောင်းကိုနားလည်လောက်ပြီဆိုတော့ Rust ထဲက __Data Types__ အကြောင်းတွေကိုဆက်လေ့လာကြည့်ရအောင်။

<hr>

[prev. Hello, World!](../CH01/part_02_hello.md)
