    You can nest Promise.props when using the Bluebird library.
    
    import Promise from "bluebird";
    
    const promiseItems = {
        letterA: Promise.resolve("letA"),
        letterB: Promise.resolve("letB"),
      };
      const fakePromise = {
        number1: Promise.resolve("num1"),
        number2: Promise.props(promiseItems),
      };
      return Promise.props(fakePromise).then((data) => {
        debugger;
        return data;
      });
