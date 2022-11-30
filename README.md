# swiftcode
variables 
```
var l : Int = 10
print(l)
l = 20
var a = 10 
a = 20
print(a)
```
constants 
let is the keyword for constants 
```
let b = 10
print(b)
```
let is a constant cant change the keyword
```
var c = 10.00
print(c)
var d : Float = 10.97393729
print(d)
```
```
var e : String = "this is how strings work"
print(e)
```
this covers how variables work in swift

    this also covers strings and integers in swift 
    multi line strings in swift
```
var f = """
    this is how
    multi line Strings work
    in swift
    """
print(f)
```
    to print multi line stirngs with out any break
    ```
var g = """
    this is how \
    multi line strings \
    works
    """
print(g)
```
    //booleans
    ```
var h : Bool = false
print(h)
```
    //string interpolation 
    ```
var i = 10
print("the value of the variable i is \(i)")
```
    string interpolation can be used to even write code inside strings
    constants is also covered
    type annontations
    type inference: Swift is able to infer the type of something based on how you created it.
    type annontations is about being explicit about the type of your data 
    ```
var str : String = "this is assigning the variable str to String type "
var j : Int = 10
```


complex data types 
arrays 
```
let john = "John Lennon"
let paul = "Paul McCartney"
let george = "George Harrison"
let ringo = "Ringo Starr"

let beatles = [john, paul, george, ringo]
print(beatles[0])
```
    //type annontations for arrays 
    ```
var arr : [Int] 
arr = [0,1,2,3,99,5,6]
print(arr[4])
```
```
var arr1 : [String]
arr1 = ["scoups","vernon","wonwoo","mingyu"]
print(arr1[1])
```
    sets
    sets use the keyword set 
    data isnt stored in a particularnorder in a set
    all the items in a set are unique
    ```
let colors = Set(["serenity ocean","rose quartz","purple","purple"])
print(colors)
    //set with type annontations
let colors2 : Set<Int> = Set([1,2,3,4,5,6,7,7,7,8,9])
print(colors2)
```
    tuples
    tuples cant be altered 
    fixed in size
    ```
let tup = (first : "jeon" , last : "wonwoo")
print(tup.last)
```
    //dictionaries 
    ```
let vocal = [
    "main1" : "seungkwan",
    "main2" : "dokyeom",
    "lead1" : "jeonghan",
    "lead2" : "joshua" ,
    "producer" : "woozi"
]
print(vocal["main1"]!)
```
    //dictionaries with type annontations 
    ```
let perf : [String : String] = [
    "main1" : "hoshi",
    "main2" : "dino",
    "lead1" : "the8",
    "lead2" : "jun"]
print(perf["main2", default : "dino"])
```
    //dictionary default values
    ```
print(perf["main",default : "dino"])
```
    //creating empty collections 
    //empty dictionary
```
var teams = [String: String]()
```
//empty array
```
var results = [Int]()
```
//empty sets
```
var words = Set<String>()
var numbers = Set([1,2,3])
```
//enumerations
//enumerations uses the enum keyword
```
enum kpop  {
    case bg
    case gg
    case mixedg
    case band
}
var type = kpop.gg
```

```
switch type {
case .bg :
    print("Seventeen,exo,bts,big bang")
case .gg :
        print("blackpink,twice,mamamoo,itzy")
    case .mixedg :
        print("kard")
        case .band :
            print("day6,xdinary heroes")
            default : 
                print("soloists like iu,ailee, leehi,punch")
}
```

```
enum kpop1 : CaseIterable {
    case bg
    case gg
    case mixedg
    case band
}
for grp in kpop1.allCases {
    print(grp)
}
```
//enum associated values 
//enum associated values is used to provide extra information about the enum cases.
```
enum boygroup {
    case seventeen, ateez(fav : String), txt, straykids, p1harmony, theboyz, exo, bts, enha
}
var bg1 = boygroup.ateez(fav : "seonghwa")
print(bg1)
```
//enum raw values
```
enum girlgroup : Int {
    case twice
    case itzy
    case nmixx
    case billlie
    case purplekiss 
}
let gg1 = girlgroup(rawValue: 0)
print(gg1!)
```
    //enum in case of switch statement 
```
enum seasons {
    case summer, winter, rainy, autumn
}
var xy = seasons.summer
xy = .winter
switch xy {
case .summer :
    print("its too sunny keep yourself hydrated")
    case .winter :
        print("its too cold, keep yourself warm")
        case .rainy :
            print("its the rainy season, keep an umbrella always with you")
            case .autumn :
                print("its the seasons of leaves on ground, be careful when you walk")
                default :
                    print("Hey!! ts spring, its the perfect weather/climate")
}
```
fallthrough in switch statements
```
enum ImageType {
    case jpeg
    case png
    case gif
}

let imageTypeToDescribe = ImageType.gif

var description = "The image type \(imageTypeToDescribe) is"

switch imageTypeToDescribe {
case .gif:
    description += " animatable, and also"
    fallthrough
default:
    description += " an image."
}

print(description) // The image type gif is animatable, and also an image.
```
