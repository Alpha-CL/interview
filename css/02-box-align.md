# box center

#### horizontal center

``` javascript
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////


.wrapper {

  height: 300px;
  border: 1px solid;

  .horizontal-center {
    margin: 0 auto;
    
    width: 100px;
  }
}


//- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -//


.wrapper {
  display: flex;
  justify-content: center;

  height: 300px;
  border: 1px solid;

  .center {
  }
}



///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
```

#### vertical center

``` javascript
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////


// 需要一个兄弟元素作为参照物

.wrapper {

  height: 300px;
  border: 1px solid;

  &:before {
    content: "";
    display: inline-block;
    vertical-align: middle;
    height: 100%;
  }

  .vertical-center {
    display: inline-block;
    vertical-align: middle;
  }
}


//- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -//


.wrapper {
  position: relative;

  height: 300px;
  border: 1px solid;

  .vertical-center {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: red;
  }
}


//- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -//


.wrapper {
  display: flex;
  flex-flow: column nowrap;
  justify-content: center;
  
  height: 300px;
  border: 1px solid;

  .vertical-center {
  }
}


///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
```

#### center

``` javascript
///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////


.wrapper {
  text-align: center;

  height: 300px;
  border: 1px solid;

  &:before {
    content: '';
    display: inline-block;
    vertical-align: middle;
    height: 100%;
  }

  .center {
    display: inline-block;
    vertical-align: middle;
    margin: 0 auto;
    background-color: red;
  }
}


//- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -//


.wrapper {
  position: relative;

  height: 300px;
  border: 1px solid;

  .center {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: red;
  }
}

//- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -//


.wrapper {
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
  align-items: center;

  height: 300px;
  border: 1px solid;

  .center {
    background-color: red;
  }
}


///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
```