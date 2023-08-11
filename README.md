# vue

## v-once

처음 랜더링 된 이후에는 데이터가 바뀌지 않는다

```markdown
<span v-once>{{ 데이터 }}<span>
```

## v-html

실제 html구조로 출력

```markdown
<div v-html="데이터">
```

## v-html

실제 html구조로 출력

```markdown
<div v-html="데이터">
```

## v-bind

html안에 속성에 이중중괄호 사용 불가  
data를 속성에서 사용하려면 v-bind 사용  
\*약어 사용 가능 (사용 비중 높음)

동적 전달인자 ' [ ] ' 안에 데이터입력

```markdown
<div v-bind:속성="데이터">

# 약어
<div :속성="데이터">

# 동적전달인자
<div :[데이터]="데이터">
```

## v-on

이벤트 실행

```markdown
<a v-on:이벤트='메소드">

# 약어
<a @이벤트='메소드">

# 동적전달인자
<div :[데이터]="메소드">
```

## computed

계산된 데이터  
computed 캐싱 : 한번 연산해놓은 값은 다시 연산하지 않고 여러번 출력 할 수 있다.

```markdown
computed : {
메소드명(){
return {

    }

}
}
```

## computed getter setter

```markdown
computed : {
  계산된 데이터: {
    get (){
      계산된 데이터가 값을 얻어내는 용도의 로직
  },
  set (매개변수){
    this.데이터 = 매개변수
    // 계산된 데이터에 어떤 값을 할당할때  
    set부분이 실행
  }
}
}
```

## watch

데이터들의 변경사항을 감시  
변경사항이 일어나면 로직 실행  
계산된 데이터도 감시 가능

```markdown
watch:{
  데이터 (){
    console.log(this.데이터)
  }
}

# 매개변수 활용가능
watch:{
  데이터 (매개변수){
    console.log(매개변수)
  }
}
```

## v-if

조건부 랜더링  
랜더링을 하지 않고 있다가 true일때 랜더링 한다.

```markdown
<div v-if="">
<div v-else-if="">
<div v-else>

<!-- <div> -->
```

## v-show

조건의 true, false와 상관 없이 랜더링 한 후 display속성 적용

```markdown
<div v-show="">

<div style="display='none'">
```

## template

template는 html에 랜더링 되지 않는다

```markdown
<template>
  <template>랜더링 X</template>
</template>
```

## 이벤트 핸들러

@이벤트

```markdown
<div @이벤트핸들러="메소드">

# 실행하는 메소드를 여러개 연결 할 때  
','로 구분하고 메소드에 '()'를 붙인다
<div @이벤트핸들러="메소드(), 메소드()">
```

## 이벤트 수식어

```markdown
# 기본동작 막기
<a @click.prevent="메소드">
= 메소드(e){
  e.preventDefault
}

# 한번만 동작
<a @click.once="메소드">

# 체이닝 가능
<a @click.prevent.once="메소드">

# 이벤트 버블링방지
<a @click.stop="메소드">
= 메소드(e){
  e.stopPropagation()
}

# 이벤트 캡쳐링
상위요소에 걸려있는 이벤트부터 실행
<a @click.capture="메소드">

상위요소에 걸려있는 이벤트만 실행
<a @click.capture.stop="메소드">

# 이벤트가 걸려있는 요소에서만 실행
<a @click.self="메소드">

# 스크롤과 로직을 분리
<div @wheel.passive="">
부하를 줄여준다  
보통의 경우 5배 이상 빨라진다

# 키입력
<input type="text" @keydown.enter="메소드">
= 메소드(e){
  if(e.key === 'Enter'){

  }
}
조건문과 동일한 역할을 한다  
수식어는 케밥케이스로 바꿔서 입력한다
체이닝 가능
<input type="text" @keydown.ctrl.shift.enter="메소드">
```
## 폼 입력 바인딩
