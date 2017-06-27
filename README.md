# things-input-field / things-textarea

## things-input-field/things-textarea is an area for entering information into a web page.

### The form interfaces the input data with the server in a json format.
Example:

```html
    <things-input-field></things-input-field>
    <things-textarea></things-textarea>
```

*****
</br></br>
### In the form, it uses things-input-field/things-textarea to interface with the server in json data.


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

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polymer-cli

And you can run it via:

    polymer serve

Once running, you can preview your element at
`http://localhost:8080/components/things-input-field/`, where `things-input-field` is the name of the directory containing it.
