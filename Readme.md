# gulp-go

[

`goapp serve / deploy` for gulp

## Install

    npm install gulp-gaegoapp

## Usage

    var gulp   = require("gulp");
    var gulpgo = require("gulp-gogaegoapp");

    var go;
    function out(prefix) {
      prefix = (prefix || "");
      return function(data) {
          console.log(prefix, data.toString());
    };
    }

gulp.task('goserve', [], function() {
    go = gulpgo.run("serve", ['build/'], {
        cwd:       __dirname,
        onStdout:  out(),
        onStderr:  out("[error]"),
        onClose:   out("close"),
        onExit:    out("exit")
    });
});



## License

MIT
