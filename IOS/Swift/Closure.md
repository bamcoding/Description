# Closure
함수는 func 키워드를 사용해서 생성
어떤 기능을 수행하는 코드 블록

함수는 클로저의 한가지 타입
1. 글로벌 함수
2. 네스티드 함수
3. 클로저 익스프레션스

**함수와 차이점**
이름이 없고 func 키워드 없이 사용할 수 있다.

# First Class Type
변수에 할당할 수 있다.
인자를 받을 수 있다.
리턴할 수 있다.

*컴플리션 블록*
*하이 오더 펑션*

**Closure Explession Syntax**
_{(parameters) -> returnType in statement}_

예제 소스)
1. Example 1
let simpleClosure = {}
simpleClosure()

2. Example 2
let simpleClosure = {
	print("Hello!")
}
simpleClosure()

3. Example 3
let inputClosure : (String) -> Void = { name in
	print("my name is \(name)!")
}
inputClosure("이근재")

4. Example 4
let retureClosure : (String) -> String = { name in 
	return "Hello \(name)~ How are you?"
}

5. Example 5
func testFunction(simpleClosure : () -> Void){
	print("testFunction")
	simpleClosure()
}

testFunction(simpleClosure : {
	print("simpleClosure")
})


6. Example 6
func testFunction(message : String, simpleClosure : (String) -> Void){
    print("testFunction \(message)...")
    simpleClosure(message)
}

testFunction(message:"이근재", simpleClosure: { message in
    print("\(message) simpleClosure")
})



var plus: (Int, Int) -> Int = {a, b in return a+b}
var result=plus(1,5)

var multiply: (Int, Int) -> Int = {$0 * $1}
result = multiply(1,5)

func operateTwoNum(a:Int,b:Int,operation:(Int,Int)->Int) -> Int {
    return operation(a,b)
}

operateTwoNum(a:6, b:1, operation: plus)

var voidClosure : () -> Void = {
    print("보이드 클로저")
}

voidClosure()


