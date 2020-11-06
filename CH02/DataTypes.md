# Data Types

Rust programming language သည် Static Typed Programming Language ဖြစ်သည့်အတွက် code ရေးသားချိန်တွင် variable များ၏ type ကို programmer နှင့် compiler မှ သိဖို့လိုအပ်ပါတယ်။

Python, JavaScript ကဲ့သို့သော Dynamic Typed Programming Language များကိုလေ့လာဖူးသူများအနေနှင့် ဤအချက်သည် အစပိုင်းတွင် အနည်းငယ် စိတ်ရှုပ်စရာဖြစ်နိုင်ပေမဲ့ သတိမထားမိသော type error များကို compile time တွင်စစ်ထုတ်နိုင်သည့်အတွက် error ရှင်းရနည်းရန်နှင့် program performance အတွက်များစွာအထောက်အကူဖြစ်တာကိုတွေ့ရမှာပါ။

ဒီအပိုင်းမှာဆိုရင် scalar types ဖြစ်တဲ့

* Integer Types
* Floating Point Types
* Character Type
* Boolean Type

compound types တွေဖြစ်တဲ့

* array
* tuple

တို့အကြောင်းကိုရှင်းပြပေးမှာဖြစ်ပါတယ်။

တခြား programming language တွေမှာ တွေ့နေကျဖြစ်တဲ့ String type ကတော့ rust မှာ collection type ဖြစ်တဲ့အတွက် အဆုံးကျမှ အကျဥ်းချုပ်ရှင်းပြပေးပါမယ်။

</br>

## Integer Types

Programming Language တွေထဲမှာမှ System Programming တွေက programmer တွေကို memory တွေကို ကိုယ်တိုင် manage ရတဲ့ အတွက် အနည်းငယ်ခက်တယ်လို့ထင်ရပေမဲ့ Computer Science ကိုလေ့လာဖို့နဲ့ performance ကောင်းတဲ့ program ရေးဖို့အတွက်အရမ်းအဆင်ပြေပါတယ်။

Rust Language ကလည်း system programming language ဖြစ်တဲ့ အတွက် programmer တွေကို ကိုယ်တိုင် memory manage ခွင့်ပေးထားပါတယ်။ ဒါကြောင့်ပဲ Rust မှာ unsign or sign 8 bits, 16 bits, 32 bits, 64 bits, 128 bits စတဲ့ integer types များစွာရှိပါတယ်။ နောက်ပြီး machine ရဲ့ architecture ကိုလိုက်ပြီး range ပြောင်းလဲနိုင်တဲ့ `usize` `isize` စတဲ့ integer types များလည်းရှိပါတယ်။

Integer types တွေအပြည့်အစုံကိုမဖော်ပြခင် Python/Js စတဲ့ Dynamic Language background ကနေလာတဲ့ programmer တွေအနေနဲ့ ဘာကြောင့် integer types တွေအရမ်းများနေရလဲဆိုပြီး စိတ်ရှုပ်လောက်မယ်ထင်ပါတယ်။ memory တွေမှာ အနည်းဆုံး unit အဖြစ် 8bits နေရာယူပါတယ်။ RGB ရဲ့ range ကို program ထဲ ထည့်ရေးမယ်ဆိုပါစို့ color တစ်ခုစီရဲ့ range က 0 ကနေ 255 အထိပဲရှိပါတယ်။ unsign 8 bits integer ရဲ့ range က 0 - 255 အထိရှိတဲ့ အတွက် Color encode ဖို့အတွက်သင့်တော်ပါတယ်။ ဒါဆို unsign 8bits intသုံးမယ်ဆိုရင် RGB သုံးခုလုံးအတွက်မှ 24bit ပဲကုန်ကျမှာပါ။ Python တို့လို programming language တွေမှာ int types နဲ့ encode မယ်ဆိုရင် Color တစ်ခုစီအတွက် 32bits သို့ 64bits ကုန်မှာပါ။ System Programming Language တွေရဲ့ advantage အနေနဲ့ Resource ကိုခြွေတာလို့ရပါမယ်။ Programming နယ်ပယ်ထဲမှာ ဘယ်ဟာမှအလကားမရပါဘူး။ Trade off အနေနဲ့ programmer က type ကို ဂရုစိုက်ရတဲ့ အတွက် နည်းနည်းပိုအလုပ်ရှုပ်ပါတယ်။ ဒါဆို ဘာကြောင့် integer types များလဲဆိုတာရှင်းလောက်ပြီထင်ပါတယ်။

ဒါဆို integer types တွေကိုအကျိုးရှိရှိအသုံးချဖို့အတွက် type တစ်ခုချင်းစီရဲ့ range ကို သိဖို့လိုပါတယ်။ unsign integer တွေကအငယ်ဆုံးအဖြစ် 0 ကနေစပြီး unsign integer တွေရဲ့ range ကိုတွက်ထုတ်ဖို့အတွက်  `(2 ^ n) - 1` ဆိုတဲ့ ပုံသေနည်းကိုသုံးရပါတယ်။ ဒါဆို 8bits unsign integer ရဲ့ အကြီးဆုံးဖြစ်နိုင်တဲ့တန်ဖိုးကိုတွက်ကြည့်ရအောင် `(2 ^ 8) - 1 = 255` ရပါလိမ့်မယ်။ 0 ကနေစရေတဲ့အတွက် ဖော်ပြနိုင်တဲ့ ဂဏန်းအရေအတွက်က 256လုံးဖြစ်ပါတယ်။ ကျန်တဲ့ unsign integer တွေရဲ့ ဖြစ်နိုင်တဲ့ အကြီးဆုံးတန်ဖိုးတွေကို ဒီပုံသေနည်းသုံးပြီးရှာနိုင်ပါတယ်။ unsigned integer တွေရဲ့ range ကိုအောက်က ဇယားမှာကြည့်နိုင်ပါတယ်။

### unsign integers

| memory size | type annotation | range                                                   |
|-------------|---------|---------------------------------------------------------|
| 8bits       | u8      | 0 to 255                                                 |
| 16bits      | u16     | 0 to 65,535                                              |
| 32bits      | u32     | 0 to 4,294,967,295                                       |
| 64bits      | u64     | 0 to 9,223,372,036,854,775,807                           |
| 128bits     | u128    | 0 to 340,282,366,920,938,463,463,374,607,431,768,211,455 |

</br>

Rust ထဲမှာအောက်ပါအတိုင်းရေးနိုင်ပါတယ်။ `_` underscore ကိုတော့ readability အတွက်အသုံးပြုနိုင်ပါတယ်။

```Rust
fn main() {

    let x: u32 = 56; // 32bits unsigned integer
    let y = 56_u32;
    let z = 1_000_000_000_u128; // 128bits unsigned integer
}
```

signed integer တွေကတော့ အပေါင်းအနှုတ်နှစ်မျိုးလုံးရှိနိုင်တဲ့ integer တွေပါ။ `1000 1001` ဆိုတဲ့ 8bits ထဲက ပထမဆုံး bit ကို အပေါင်းနှုတ်ခွဲဖို့အတွက်သုံးပါတယ်။ ဒါကြောင့် 8bits integer မှာဆိုရင် sign အတွက် 1bit ကိုသုံးလိုက်ရတဲ့အတွက်ကြောင့် ဂဏန်းအနေနဲ့ ဖော်ပြလို့ရတာ 7 bits ပဲကျန်ပါတယ်။ signed integer မှာ အကြီးဆုံးဖြစ်နိုင်တဲ့ ကိန်းကို `(2 ^ (n - 1)) -1` ဆိုတဲ့ ပုံသေနည်းနဲ့ တွက်ထုတ်နိုင်ပါတယ်။ အငယ်ဆုံးဖြစ်နိုင်တဲ့ ကိန်းကိုတွက်ထုတ်ဖို့အတွက် `-(2 ^ (n - 1))` ဆိုတဲ့ ပုံသေနည်းကိုသုံးနိုင်ပါတယ်။ 8bit integer မှာဆိုရင် range က -128 ကနေ 127 ကြားမှာဖြစ်ပါတယ်။ signed integer တွေရဲ့ range ကိုအောက်က ဇယားမှာကြည့်နိုင်ပါတယ်။

### Signed Integers

| memory size | symbols | range                                                                                                         |
|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| 8bits       | i8      | -128 to 127                                                                                                   |
| 16bits      | i16     | −32,768 to 32,767                                                                                             |
| 32bits      | i32     | -2,147,483,648 to 2,147,483,647                                                                               |
| 64bits      | i64     | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807                                                       |
| 128bits     | i128    | −170,141,183,460,469,231,731,687,303,715,884,105,728  to  170,141,183,460,469,231,731,687,303,715,884,105,727 |

 </br>

> signed integer တွေမှာ ပထမဆုံး bit ကို လက္ခဏာသတ်မှတ်ဖို့ အတွက်ဆိုတာက အလွယ်မှတ်ဖို့ပြောတာဖြစ်ပါတယ်။ တကယ့် binary representation မှာက two's complement နည်းကိုသုံးပြီး encode ထားတာပဲဖြစ်ပါတယ်။

အပေါ်က integer types တွေအပြင် rust မှာ machine ရဲ့ 32bits, 64bits စတဲ့ architecture အလိုက်ပြောင်းနိုင်တဲ့ လကွဏာပါတဲ့ `isize` နဲ့ လကွဏာမပါတဲ့ `usize` integer types တွေလည်းရှိပါတယ်။ ဒီ integer types တွေကိုတော့ array indexing အတွက်တွေ string length စတဲ့ address နဲ့ဆိုင်တဲ့ နေရာတွေမှာသုံးပါတယ်
