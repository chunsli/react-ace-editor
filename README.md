# REACT-ACE-EDITOR

## Introduction
This is a react wrapper around the [Ace Editor](https://ace.c9.io)
[Ace Editor Demo](https://ace.c9.io/build/kitchen-sink.html)
[Ace Editor Github](https://github.com/ajaxorg/ace)

## Getting Started
```
npm install --save react-ace-editor
```

## Usage

```
import ReactAce from 'react-ace-editor';
import React, { Component } from 'react';

class CodeEditor extends Component {
  contructor() {
    super();
    this.onChange = this.onChange.bind(this);
  }
  onChange(newValue, e) {
    console.log(newValue, e);

    const editor = this.ace.editor; // The editor object is from Ace's API
    console.log(editor.getValue()); // Outputs the value of the editor
  }
  render() {
    return (
      <ReactAce
        mode="javascript"
        theme="eclipse"
        setReadOnly=false
        onChange={this.onChange}
        style={{ height: '400px' }}
        ref={instance => { this.ace = instance; }} // Let's put things into scope
      />
    );
  }
}
```

## More Documentation
For all the available method from the Ace Editor, please checkout [Ace Editor's API documentation](https://ace.c9.io/#nav=api&api=editor)


