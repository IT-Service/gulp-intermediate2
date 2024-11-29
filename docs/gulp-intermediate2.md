<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [gulp-intermediate2](./gulp-intermediate2.md)

## gulp-intermediate2 package

## Functions

<table><thead><tr><th>

Function


</th><th>

Description


</th></tr></thead>
<tbody><tr><td>

[intermediate2(process, pluginOptions)](./gulp-intermediate2.intermediate2.md)


</td><td>

Plugin fabric function.

A gulp helper for tools that need files on disk.

Some tools require access to files on disk instead of working with `stdin` and `stdout` (e.g., [Jekyll](http://jekyllrb.com/)<!-- -->, [Ruby Sass](http://sass-lang.com/)<!-- -->). `gulp-intermediate2` is a convenience plugin that writes the current `Vinyl` stream to a temporary directory, lets You run commands on the file system, and pushes the results back into the pipe.

Returns Gulp stream.

`intermediate2` writes (with `gulp.dest()`<!-- -->) input `Vinyl` file objects to [container](./gulp-intermediate2.intermediate2options.container.md) subdirectory in temporary directory under system `Temp`<!-- -->.

After all files are written, `intermediate2` run [process](./gulp-intermediate2.process.md) and wait for it finish.

[Process](./gulp-intermediate2.process.md) must be read files from `srcDirPath` directory ([pluginOptions.container](./gulp-intermediate2.intermediate2options.container.md) temp directory), and write output files to `destDirPath` ([pluginOptions.output](./gulp-intermediate2.intermediate2options.output.md) temp directory).

After that `intermediate2` will read files (with `gulp.src()`<!-- -->) from [pluginOptions.output](./gulp-intermediate2.intermediate2options.output.md) directory and will push they to gulp stream.


</td></tr>
</tbody></table>

## Interfaces

<table><thead><tr><th>

Interface


</th><th>

Description


</th></tr></thead>
<tbody><tr><td>

[Intermediate2Options](./gulp-intermediate2.intermediate2options.md)


</td><td>

gulp-intermediate2 plugin options


</td></tr>
</tbody></table>

## Type Aliases

<table><thead><tr><th>

Type Alias


</th><th>

Description


</th></tr></thead>
<tbody><tr><td>

[Process](./gulp-intermediate2.process.md)


</td><td>

[intermediate2()](./gulp-intermediate2.intermediate2.md) Process function.

Process started after input files written to `srcDirPath` directory ([pluginOptions.container](./gulp-intermediate2.intermediate2options.container.md) temp directory).

Process must write output files to `destDirPath` ([pluginOptions.output](./gulp-intermediate2.intermediate2options.output.md) temp directory).

After the process is completed, it need to call a callback. Or process function can return `ChildProcess`<!-- -->, `EventEmitter`<!-- -->, `Observable<R>`<!-- -->, `PromiseLike<R>`<!-- -->, `Stream` object. `intermediate2` await processes, represented by returned object.

After process finished, result files pushed to output stream.


</td></tr>
<tr><td>

[ProcessCallback](./gulp-intermediate2.processcallback.md)


</td><td>

[intermediate2()](./gulp-intermediate2.intermediate2.md) [Process](./gulp-intermediate2.process.md) function callback


</td></tr>
</tbody></table>