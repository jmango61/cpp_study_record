# cpp_study_record
## c++ 스터디 1주차_구지민
---
### 1. 기초 복습
```c++
#include <iostream>
using namespace std;    // <iostream> 헤더 파일에 선언된 이름을 사용할 때 std:: 생략
  
  int main(){ // c++ 프로그램은 main() 함수에서부터 실행을 시작함.
 
 cout << "Hello\n";    // \n과 endl은 다음줄로 넘어가는 역할
 
 cout << "첫 번째 예제입니다.";
  
  return 0;     // main() 함수가 종료하면 프로그램이 종료됨
  }
  ```
  
  - `# include <iostream>`
  은 **전처리기에 대한 지시문**  
  : c++ 소스파일을 컴파일하기 전에 <iostream> 헤더 파일을 읽어 C++ 소스 파일 안에 삽입할 것을 지시  
  
  
 ### 2. 키 입력 받기  
  
  - `cin >>` 은 키 입력  
  >여러 개의 `>>`연산자를 이용하여 여러 값을 입력받을 수도 있음
  
  - `Enter`키를 입력해야 `>>`연산자가 작동함
  
  - `bool, char, short, int, long, float, double`와 같은 모든 기본 타입에 대해 `>>` 연산자로 데이터 입력이 가능함  
  
  #### 2-1. 키보드에서 문자열 입력받고 출력
  
 > C++의 문자열  
    
>>  (1) C-스트링 
  
  ```c++
  #include <iostream>
  using namespace stdl
  
  int main(){
  cout << "이름을 입력하세요 >>";
  
  char name[11];  // 한글은 5개 글자, 영문은 10까지 저장할 수 있음
  cin >> name; // 키보드로부터 문자열을 읽음
  
  cout << "이름은" << name << "입니다\n"; // 이름을 출력함
  }
  ```
  
  ```c++
  이름을 입력하세요 >> 마이클
  이름은 마이클입니다
  ```
    
    
>>  **(2) string 클래스 (권장)**  
  - 문자열 크기 제약이 없으므로 다루기 쉬움  
    
  ```C++
  #include <iostream>
  #include <string>   // string 클래스를 사용하기 위한 헤더 파일 
  using namespace std;
  
  int main(){
    string song("Falling in love with you");  // 문자열 song
    string elvis("Elvis Presley");    // 문자열 elvis
    string singer;    // 문자열 singer
  
    cout << song + "를 부른 가수는";    // +로 문자열 연결
    cout << "(힌트 : 첫 글자는 " << elvis[0] << ")?";   // [] 연산자 사용
  
    getline(cin, siger);    // 문자열 입력. getline()은 string 타입의 c++ 문자열을 입력 받기 위해 제공되는 전역 함수. 빈칸을 포함하는 문자열 입력 가능 ! 
    if(singr == elvis)    // 문자열 비교
      cout << "맞았습니다.";
    else
      cout << "틀렸습니다." + elvis + "입니다." << endl;    // +로 문자열 연결 
  }
  ```
  
  ```c++
  Falling in love with you를 부른 가수는(힌트 : 첫글자는 E)?Elvis Pride  //빈칸포함
  틀렸습니다. Elvis Presley입니다.
  ```
    
  
  ** `getline()` 멤버 함수는 공백이 포함된 문자열을 입력**
  
     
  
  
  
