# 스트림 API

Stream
- sequence of elements
- 데이터를 담고 있는 저장소(컬렉션)이 아니다.
- Functional in nature, 스트림이 처리하는 데이터 소스를 변경하지 않는다.
- 스트림으로 처리하는 데이터는 오직 한번만 처리한다.
- 무제한일 수도 있다. (Short Circuit 메소드를 사용해서 제한할 수 있다.)
- 중개 오퍼레이션은 근본적으로 lazy 하다. 
- 손쉽게 병렬 처리할 수 있다. (데이터가 정말 방대할 경우에 사용할 수 있다.)

스트림 파이프라인
- 0 또는 다수의 중개 오퍼레이션 (intermediate operation)과 한개의 종료 오퍼레이션(terminal operation)으로 구성한다.
- 스트림의 데이터 소스는 오직 터미널 오퍼레이션을 실행할 때에만 처리한다.

중개 오퍼레이션
- Stream을 리턴한다.
- Stateless / Stateful 오퍼레이션으로 더 상세하게 구분할 수도 있다.(대부분은 Stateless지만 distinct나 sorted 처럼 이전 소스 데이터를 참조해야 하는 오퍼레이션은 Stateful오퍼레이션이다.)
-filter, map, limit, skip, sorted

종료 오퍼레이션
- Stream을 리턴하지 않는다.
- collect, allMatch, count, forEach, min, max ...


연속된 데이터를 처리하는 오퍼레이션의 모음


소스를 변경하지 않는다.

```
List<String> list = new ArrayList<>();
list.add("lee");
list.add("sin");
list.add("kim");
list.add("park");

Stream<String> stringStream = names.stream().map(String::toUpperCase);
```


중계 오퍼레이션은 레이지하다.
- map

종료 오퍼레이션
- collect 