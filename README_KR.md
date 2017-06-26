# things-input-field / things-textarea

## things-input-field/things-textarea는 웹 페이지로 정보를 입력하는 영역이다.

### form은 json 형식을 통하여 서버와 input data를 인터페이스한다.
Example:

```html
    <things-input-field></things-input-field>
    <things-textarea></things-textarea>
```

*****
</br></br>
### form에서 things-input-field/things-textarea를 사용하여 json data로 서버와 인터페이스한다.

Example:

```html

    <form is="iron-form" id="form"  >
      <things-input-field name="firstName"
          label="FirstName:"
          id="input1"
          value></things-input-field>
      <things-input-field name="lastName"
          label="LastName:"
          id="input2"></things-input-field>
      <things-input-field name="eMail"
          label="E-Mail:"
          id="input3"></things-input-field>
      <things-input-field name="description"
          label="Description:"
          id="input3"></things-input-field>
      <things-textarea  name="sampletextarea"
               label="TextArea:"
              id="input2"></things-textarea>

    </form>
    <button class="button" on-tap="submit">Submit</button><br><br>
  <script>
    Polymer({
      is: 'sample-input-field',
      submit: function(){
        this.$.p1.innerHTML = JSON.stringify(this.$.form.serialize());
      }
    });
  </script>
```

## Dependencies

element의 종속성은 [Bower](http://bower.io/)를 통해 관리되며, 아래의 방법을 통해 설치할 수 있다.

    npm install -g bower

다음, element의 종속성을 다운로드한다.

    bower install

## Playing With Your Element

element를 독립적으로 처리하려면 [Polyserve](https://github.com/PolymerLabs/polyserve)를 사용하여 element의 bower 의존성을 유지하도록 하며, 이는 아래의 방법을 통해 설치할 수 있다.

    npm install -g polymer-cli

그리고, 아래의 방법을 통해 실행할 수 있다.

    polymer serve

element를 실행한 경우, `things-alarm`이 디렉토리 이름으로 포함되어 있는 `http://localhost:8080/components/things-alarm/`를 통해 이를 미리 확인할 수 있다. 
