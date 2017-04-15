# api documentation for  [gulp-git (v2.1.0)](http://github.com/stevelacy/gulp-git)  [![npm package](https://img.shields.io/npm/v/npmdoc-gulp-git.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-gulp-git) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-gulp-git.svg)](https://travis-ci.org/npmdoc/node-npmdoc-gulp-git)
#### Git plugin for gulp (gulpjs.com)

[![NPM](https://nodei.co/npm/gulp-git.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/gulp-git)

[![apidoc](https://npmdoc.github.io/node-npmdoc-gulp-git/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-gulp-git/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-gulp-git/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-gulp-git/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Steve Lacy me@slacy.me",
        "url": "slacy.me"
    },
    "bugs": {
        "url": "https://github.com/stevelacy/gulp-git/issues"
    },
    "dependencies": {
        "any-shell-escape": "^0.1.1",
        "gulp-util": "^3.0.8",
        "require-dir": "^0.3.1",
        "strip-bom-stream": "^3.0.0",
        "through2": "^2.0.3",
        "vinyl": "^2.0.1"
    },
    "description": "Git plugin for gulp (gulpjs.com)",
    "devDependencies": {
        "eslint": "^3.17.0",
        "mocha": "^3.2.0",
        "rimraf": "^2.6.1",
        "should": "^11.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "f09661529e4e15626b6dae7d330820d9871f9d65",
        "tarball": "https://registry.npmjs.org/gulp-git/-/gulp-git-2.1.0.tgz"
    },
    "engines": {
        "node": ">= 0.9.0"
    },
    "gitHead": "7894cdd4629c2d86626eed14ebb31ecb95edcb35",
    "homepage": "http://github.com/stevelacy/gulp-git",
    "keywords": [
        "gulp",
        "git",
        "gulpgit",
        "gulpplugin",
        "gulp-plugin"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "stevelacy"
        }
    ],
    "name": "gulp-git",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/stevelacy/gulp-git.git"
    },
    "scripts": {
        "docs": "rimraf docs/* && jsdoc ./index.js ./lib --recurse --destination ./docs",
        "pretest": "rimraf test/repo test/tmp && eslint ./index.js ./examples/ ./lib/ ./test/",
        "test": "mocha --reporter spec --timeout 6000 test/main.js"
    },
    "version": "2.1.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module gulp-git](#apidoc.module.gulp-git)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>add (opt)](#apidoc.element.gulp-git.add)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>addRemote (remote, url, opt, cb)](#apidoc.element.gulp-git.addRemote)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>addSubmodule (url, name, opt, cb)](#apidoc.element.gulp-git.addSubmodule)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>branch (branch, opt, cb)](#apidoc.element.gulp-git.branch)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>catFile (opt)](#apidoc.element.gulp-git.catFile)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>checkout (branch, opt, cb)](#apidoc.element.gulp-git.checkout)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>checkoutFiles (opt)](#apidoc.element.gulp-git.checkoutFiles)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>clean (paths, opt, cb)](#apidoc.element.gulp-git.clean)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>clone (remote, opt, cb)](#apidoc.element.gulp-git.clone)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>commit (message, opt)](#apidoc.element.gulp-git.commit)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>diff (compare, opt)](#apidoc.element.gulp-git.diff)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>exec (opt, cb)](#apidoc.element.gulp-git.exec)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>fetch (remote, branch, opt, cb)](#apidoc.element.gulp-git.fetch)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>init (opt, cb)](#apidoc.element.gulp-git.init)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>merge (branch, opt, cb)](#apidoc.element.gulp-git.merge)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>pull (remote, branch, opt, cb)](#apidoc.element.gulp-git.pull)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>push (remote, branch, opt, cb)](#apidoc.element.gulp-git.push)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>removeRemote (remote, opt, cb)](#apidoc.element.gulp-git.removeRemote)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>reset (commit, opt, cb)](#apidoc.element.gulp-git.reset)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>revParse (opt, cb)](#apidoc.element.gulp-git.revParse)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>rm (opt)](#apidoc.element.gulp-git.rm)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>stash (opt, cb)](#apidoc.element.gulp-git.stash)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>status (opt, cb)](#apidoc.element.gulp-git.status)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>tag (version, message, opt, cb)](#apidoc.element.gulp-git.tag)
1.  [function <span class="apidocSignatureSpan">gulp-git.</span>updateSubmodule (opt, cb)](#apidoc.element.gulp-git.updateSubmodule)



# <a name="apidoc.module.gulp-git"></a>[module gulp-git](#apidoc.module.gulp-git)

#### <a name="apidoc.element.gulp-git.add"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>add (opt)](#apidoc.element.gulp-git.add)
- description and source-code
```javascript
add = function (opt) {
  if (!opt) opt = {};
  if (!opt.args) opt.args = ' ';

  var paths = [];
  var files = [];
  var fileCwd = process.cwd;

  var write = function(file, enc, cb) {
    paths.push(file.path);
    files.push(file);
    fileCwd = file.cwd;
    cb();
  };

  var flush = function(cb) {
    var cwd = opt.cwd || fileCwd;

    var cmd = 'git add ' + escape(paths) + ' ' + opt.args;
    var that = this;
    var maxBuffer = opt.maxBuffer || 200 * 1024;

    exec(cmd, {cwd: cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
      if (err) cb(err);
      if (!opt.quiet) gutil.log(stdout, stderr);
      files.forEach(that.push.bind(that));
      that.emit('end');
      cb();
    });
  };

  return through.obj(write, flush);
}
```
- example usage
```shell
...
  });
});

// Run git add
// src is the file(s) to add (or ./*)
gulp.task('add', function(){
  return gulp.src('./git-test/*')
    .pipe(git.add());
});

// Run git add with options
gulp.task('add', function(){
  return gulp.src('./git-test/*')
    .pipe(git.add({args: '-f -i -p'}));
});
...
```

#### <a name="apidoc.element.gulp-git.addRemote"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>addRemote (remote, url, opt, cb)](#apidoc.element.gulp-git.addRemote)
- description and source-code
```javascript
addRemote = function (remote, url, opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!url) cb(new Error('gulp-git: Repo URL is required git.addRemote("origin", "https://github.com/user/repo.git")'));
  if (!remote) remote = 'origin';
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git remote add ' + opt.args + ' ' + escape([remote, url]);
  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb();
  });
}
```
- example usage
```shell
...
    });
});

// Run git remote add
// remote is the remote repo
// repo is the https url of the repo
gulp.task('addremote', function(){
  git.addRemote('origin', 'https://github.com/stevelacy/git-test', function (err) {
    if (err) throw err;
  });
});

// Run git remote remove
// remote is the remote repo
gulp.task('removeremote', function(){
...
```

#### <a name="apidoc.element.gulp-git.addSubmodule"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>addSubmodule (url, name, opt, cb)](#apidoc.element.gulp-git.addSubmodule)
- description and source-code
```javascript
addSubmodule = function (url, name, opt, cb) {
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!url) cb(new Error('gulp-git: Repo URL is required git.submodule.add("https://github.com/user/repo.git", "repoName")'));
  if (!name) name = '';
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = '';

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git submodule add ' + opt.args + ' ' + url + ' ' + name;
  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err && cb) cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    if (cb) cb();
  });
}
```
- example usage
```shell
...
// Git rm a file or folder
gulp.task('rm', function(){
  return gulp.src('./gruntfile.js')
    .pipe(git.rm());
});

gulp.task('addSubmodule', function(){
  git.addSubmodule('https://github.com/stevelacy/git-test', 'git-test', { args: '-b master'});
});

gulp.task('updateSubmodules', function(){
  git.updateSubmodule({ args: '--init' });
});

// Working tree status
...
```

#### <a name="apidoc.element.gulp-git.branch"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>branch (branch, opt, cb)](#apidoc.element.gulp-git.branch)
- description and source-code
```javascript
branch = function (branch, opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!branch) return cb(new Error('gulp-git: Branch name is required git.branch("name")'));
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git branch ' + opt.args + ' ' + escape([branch]);
  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb();
  });
}
```
- example usage
```shell
...
git.tag('v1.1.1', 'Version message with signed key', {signed: true}, function (err) {
  if (err) throw err;
});
});

// Create a git branch
gulp.task('branch', function(){
git.branch('newBranch', function (err) {
  if (err) throw err;
});
});

// Checkout a git branch
gulp.task('checkout', function(){
git.checkout('branchName', function (err) {
...
```

#### <a name="apidoc.element.gulp-git.catFile"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>catFile (opt)](#apidoc.element.gulp-git.catFile)
- description and source-code
```javascript
catFile = function (opt) {
  if (!opt) opt = {};
  if (undefined === opt.stripBOM || null === opt.stripBOM) opt.stripBOM = true;
  if (undefined === opt.buffer || null === opt.buffer) opt.buffer = true;

<span class="apidocCodeCommentSpan">  /**
   * transform function of stream {@link https://nodejs.org/docs/latest/api/stream.html#stream_transform_transform_chunk_encoding_callback
}
   *
   * @param {vinyl}    file The file to be transformed.
   * @param {any}      enc  encoding type.
   * @param {function} cb   A callback function (optionally with an error argument and data) to be called after the supplied 'file
' has been processed.
   * @returns {void}
   */
</span>  var write = function(file, enc, cb) {

    var hash = file.git && file.git.hash;

    /**
     * set file contents and send file to stream
     *
     * @param {Buffer} contents file contents
     * @returns {void}
     */
    var sendFile = function(contents) {
      if (contents) {
        file.contents = contents;
      }
      return cb(null, file);
    };

    if (!hash || /^0+$/.test(hash)) {
      return sendFile();
    }

    var catFile = spawn('git', ['cat-file', 'blob', hash], {
      cwd: file.cwd
    });

    var contents = catFile.stdout;
    var that = this;

    readStream(catFile.stderr, function(error) {
      that.emit('error', new gutil.PluginError('gulp-git', 'Command failed: ' + catFile.spawnargs.join(' ').trim() + '\n' + error
.toString()));
    });

    if (opt.stripBOM) {
      contents = contents.pipe(stripBom());
    }

    if (opt.buffer) {
      readStream(contents, sendFile);
    } else {
      sendFile(contents);
    }
  };
  var stream = through.obj(write);
  return stream;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-git.checkout"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>checkout (branch, opt, cb)](#apidoc.element.gulp-git.checkout)
- description and source-code
```javascript
checkout = function (branch, opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!branch) throw new Error('gulp-git: Branch name is require git.checkout("name")');
  if (!opt.args) opt.args = ' ';
  if (!opt.cwd) opt.cwd = process.cwd();

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git checkout ' + opt.args + ' ' + escape([branch]);
  exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb(null);
  });
}
```
- example usage
```shell
...
git.branch('newBranch', function (err) {
  if (err) throw err;
});
});

// Checkout a git branch
gulp.task('checkout', function(){
git.checkout('branchName', function (err) {
  if (err) throw err;
});
});

// Create and switch to a git branch
gulp.task('checkout', function(){
git.checkout('branchName', {args:'-b'}, function (err) {
...
```

#### <a name="apidoc.element.gulp-git.checkoutFiles"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>checkoutFiles (opt)](#apidoc.element.gulp-git.checkoutFiles)
- description and source-code
```javascript
checkoutFiles = function (opt) {
  if (!opt) opt = {};
  if (!opt.args) opt.args = ' ';

  function checkout(file, enc, cb) {
    var that = this;
    var cmd = 'git checkout ' + opt.args + ' ' + escape([file.path]);
    if (!cb || typeof cb !== 'function') cb = function () {};

    var maxBuffer = opt.maxBuffer || 200 * 1024;

    exec(cmd, {cwd: file.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
      if (err) return cb(err);
      if (!opt.quiet) gutil.log(stdout, stderr);
      that.push(file);
      cb(null);
    });
  }

  // Return a stream
  return through.obj(checkout);
}
```
- example usage
```shell
...
});
'''

If you want to checkout files (e.g. revert them) use git.checkoutFiles:

'''js
gulp.src('./*')
  .pipe(git.checkoutFiles());
'''

### git.checkoutFiles(opt)
'git checkout <list of files>'

Checkout (e.g. reset) files
...
```

#### <a name="apidoc.element.gulp-git.clean"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>clean (paths, opt, cb)](#apidoc.element.gulp-git.clean)
- description and source-code
```javascript
clean = function (paths, opt, cb) {
  if (!cb) {
    if (typeof opt === 'function') {
      // passed in 2 arguments
      cb = opt;
      if (typeof paths === 'object') {
        opt = paths;
        paths = '';
      }
      else opt = {};
    }
    else {
      // passed in only cb
      cb = paths;
      paths = '';
      opt = {};
    }
  }

  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';

  var cmd = 'git clean ' + opt.args + ' ' + (paths.trim() ? (' -- ' + escape(paths)) : '');

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  return exec(cmd, { cwd: opt.cwd, maxBuffer: maxBuffer }, function (err, stdout, stderr) {
    if (err)
      return cb(err);
    if (!opt.quiet)
      gutil.log(stdout, stderr);
    cb();
  });
}
```
- example usage
```shell
...
  git.exec({args : 'log --follow index.js'}, function (err, stdout) {
    if (err) throw err;
  });
});

// Git clean files
gulp.task('clean', function() {
  git.clean({ args: '-f' }, function (err) {
    if(err) throw err;
  });
});

// Run gulp's default task
gulp.task('default',['add']);
'''
...
```

#### <a name="apidoc.element.gulp-git.clone"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>clone (remote, opt, cb)](#apidoc.element.gulp-git.clone)
- description and source-code
```javascript
clone = function (remote, opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git clone ' + escape([remote]) + ' ' + opt.args;
  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb();
  });
}
```
- example usage
```shell
...
git.fetch('origin', '', function (err) {
  if (err) throw err;
});
});

// Clone a remote repo
gulp.task('clone', function(){
git.clone('https://github.com/stevelacy/gulp-git', function (err) {
  if (err) throw err;
});
});

// Clone remote repo to sub folder ($CWD/sub/folder/git-test)
gulp.task('clonesub', function() {
git.clone('https://github.com/stevelacy/git-test', {args: './sub/folder'}, function(err) {
...
```

#### <a name="apidoc.element.gulp-git.commit"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>commit (message, opt)](#apidoc.element.gulp-git.commit)
- description and source-code
```javascript
commit = function (message, opt) {
  if (!opt) opt = {};
  if (!message || message.length === 0) {
    if (opt.args.indexOf('--amend') === -1 && opt.disableMessageRequirement !== true) {
      throw new Error('gulp-git: Commit message is required git.commit("commit message") or --amend arg must be given');
    }
  }
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.maxBuffer) opt.maxBuffer = 200 * 1024; // Default buffer value for child_process.exec
  if (!opt.args) opt.args = ' ';

  var files = [];
  var paths = [];

  var write = function(file, enc, cb) {
    files.push(file);
    paths.push(path.relative(opt.cwd, file.path).replace('\\', '/'));
    cb();
  };

  var messageEntry = function(entry) {
    return '-m "' + entry + '" ';
  };

  var flush = function(cb) {
    var writeStdin = false;
    var cmd = 'git commit ';

    if (message && opt.args.indexOf('--amend') === -1) {

      // Check if the message is multiline
      if (message && message instanceof Array) {

        if (opt.multiline) {
          writeStdin = true;
          message = message.join('\n');
        } else {
          var messageExpanded = '';

          // repeat -m as needed
          for (var i = 0; i < message.length; i++) {
            messageExpanded += messageEntry(message[i]);
          }
          cmd += messageExpanded + opt.args;
        }
        if (!opt.disableAppendPaths) {
          cmd += ' ' + escape(paths);
        }
      } else {
        if (~message.indexOf('\n')) {
          writeStdin = true;
        } else {
          cmd += '-m "' + message + '" ' + opt.args;
        }
        if (!opt.disableAppendPaths) {
          cmd += ' ' + escape(paths);
        }
      }
    } else if (opt.disableMessageRequirement === true) {
      cmd += opt.args;
    } else {
      // When amending, just add the file automatically and do not include the message not the file.
      // Also, add all the files and avoid lauching the editor (even if --no-editor was added)
      cmd += '-a ' + opt.args + (opt.args.indexOf('--no-edit') === -1 ? ' --no-edit' : '');
    }
    var self = this;

    // If 'message' was an array and 'opt.multiline' was true
    // or was a string containing newlines, we append '-F -'
    if (writeStdin) {
      cmd += ' -F -';
    }

    var execChildProcess = exec(cmd, opt, function(err, stdout, stderr) {
      if (err && (String(stdout).indexOf('no changes added to commit') === 0)) return cb(err);
      if (!opt.quiet) gutil.log(stdout, stderr);
      files.forEach(self.push.bind(self));
      self.emit('end');
      return cb();
    });

    if (writeStdin) {
      execChildProcess.stdin.write(message);
      execChildProcess.stdin.end();
    }

    // If the user wants, we'll emit data events during exec
    // they can listen to them with .on('data',function(data){ });
    // in their task
    if (opt.emitData) {
      execChildProcess.stdout.on('data', function(data) {
        self.emit('data', data);
      });
      execChildProcess.stderr.on('data', function(data) {
        self.emit('data', data);
      });
    }
  };

  return through.obj(write, flush);
}
```
- example usage
```shell
...
    .pipe(git.add({args: '-f -i -p'}));
});

// Run git commit
// src are the files to commit (or ./*)
gulp.task('commit', function(){
  return gulp.src('./git-test/*')
    .pipe(git.commit('initial commit'));
});

// Run git commit with options
gulp.task('commit', function(){
  return gulp.src('./git-test/*')
    .pipe(git.commit('initial commit', {args: '-A --amend -s'}));
});
...
```

#### <a name="apidoc.element.gulp-git.diff"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>diff (compare, opt)](#apidoc.element.gulp-git.diff)
- description and source-code
```javascript
diff = function (compare, opt) {
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  // https://github.com/gulpjs/vinyl-fs#optionsread
  if (undefined === opt.read || null === opt.read) opt.read = true;
  if (undefined === opt.log || null === opt.log) opt.log = true;

  var srcStream = through.obj();
  var cmd = compare;

  if (!/--diff-filter=/.test(opt.args)) {
    cmd += ' --diff-filter=ACM';
  }
  if (opt.args) {
    cmd += ' ' + opt.args;
  }
  exec('git diff --raw -z ' + cmd, {cwd: opt.cwd}, function(err, stdout) {
    if (err) return srcStream.emit('error', err);
    var files = getReaslt(stdout);

    if (opt.log) {
      gutil.log('git diff --name-status ' + cmd + '\n' + files.map(function(diff) {
        return diff.status + '\t' + diff.dstPath;
      }).join('\n'));
    }

    files.forEach(function(diff) {
      srcStream.write(new Vinyl({
        path: path.resolve(opt.cwd, diff.dstPath),
        cwd: opt.cwd,
        base: opt.base,
        git: {
          hash: diff.dstHash,
          diff: diff
        }
      }));
    });
    srcStream.end();
  });

  if (opt.read) {
    // read file contents when opt.read is 'true'
    return srcStream.pipe(catFile(opt));
  }

  return srcStream;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-git.exec"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>exec (opt, cb)](#apidoc.element.gulp-git.exec)
- description and source-code
```javascript
exec = function (opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = { };
  if (!opt.log) opt.log = !cb;
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.maxBuffer) opt.maxBuffer = 200 * 1024; // Default buffer value for child_process.exec

  if (!opt.args) opt.args = ' ';

  var cmd = 'git ' + opt.args;
  return exec(cmd, {cwd : opt.cwd, maxBuffer: opt.maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err, stderr);
    if (opt.log && !opt.quiet) gutil.log(cmd + '\n' + stdout, stderr);
    else {
      if (!opt.quiet) gutil.log(cmd + ' (log : false)', stderr);
    }
    cb(err, stdout);
  });
}
```
- example usage
```shell
...
git.status({args: '--porcelain'}, function (err, stdout) {
  if (err) throw err;
});
});

// Other actions that do not require a Vinyl
gulp.task('log', function(){
git.exec({args : 'log --follow index.js'}, function (err, stdout) {
  if (err) throw err;
});
});

// Git clean files
gulp.task('clean', function() {
git.clean({ args: '-f' }, function (err) {
...
```

#### <a name="apidoc.element.gulp-git.fetch"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>fetch (remote, branch, opt, cb)](#apidoc.element.gulp-git.fetch)
- description and source-code
```javascript
fetch = function (remote, branch, opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!branch) branch = '';
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';
  if (!remote && opt.args.indexOf('--all') === -1) remote = 'origin';

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git fetch ' + opt.args;
  var args = [];
  if (remote)
    args.push(remote);
  if (branch)
    args = args.concat(branch);
  if (args.length > 0)
    cmd += escape(args);
  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb();
  });
}
```
- example usage
```shell
...
    if (err) throw err;
  });
});

// Run git fetch
// Fetch refs from all remotes
gulp.task('fetch', function(){
  git.fetch('', '', {args: '--all'}, function (err) {
    if (err) throw err;
  });
});

// Run git fetch
// Fetch refs from origin
gulp.task('fetch', function(){
...
```

#### <a name="apidoc.element.gulp-git.init"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>init (opt, cb)](#apidoc.element.gulp-git.init)
- description and source-code
```javascript
init = function (opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git init ' + opt.args;
  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb();
  });

}
```
- example usage
```shell
...
'''javascript
var gulp = require('gulp');
var git = require('gulp-git');

// Run git init
// src is the root folder for git to initialize
gulp.task('init', function(){
git.init(function (err) {
  if (err) throw err;
});
});

// Run git init with options
gulp.task('init', function(){
git.init({args: '--quiet --bare'}, function (err) {
...
```

#### <a name="apidoc.element.gulp-git.merge"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>merge (branch, opt, cb)](#apidoc.element.gulp-git.merge)
- description and source-code
```javascript
merge = function (branch, opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!branch) return cb && cb(new Error('gulp-git: Branch name is require git.merge("name")'));
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git merge ' + opt.args + ' ' + escape([branch]);
  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb();
  });
}
```
- example usage
```shell
...
git.checkout('branchName', {args:'-b'}, function (err) {
  if (err) throw err;
});
});

// Merge branches to master
gulp.task('merge', function(){
git.merge('branchName', function (err) {
  if (err) throw err;
});
});

// Reset a commit
gulp.task('reset', function(){
git.reset('SHA', function (err) {
...
```

#### <a name="apidoc.element.gulp-git.pull"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>pull (remote, branch, opt, cb)](#apidoc.element.gulp-git.pull)
- description and source-code
```javascript
pull = function (remote, branch, opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';

  var cmd = 'git pull ' + opt.args;
  if (typeof remote === 'string') {
    cmd += ' ' + escape(remote);
  }
  if (branch && typeof branch === 'string' || branch && branch[0]) {
    cmd +=  ' ' + escape([].concat(branch));
  }
  var maxBuffer = opt.maxBuffer || 200 * 1024;

  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb();
  });
}
```
- example usage
```shell
...
});
});

// Run git pull
// remote is the remote repo
// branch is the remote branch to pull from
gulp.task('pull', function(){
git.pull('origin', 'master', {args: '--rebase'}, function (err) {
  if (err) throw err;
});
});

// Run git pull from multiple branches
gulp.task('pull', function(){
git.pull('origin', ['master', 'develop'], function (err) {
...
```

#### <a name="apidoc.element.gulp-git.push"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>push (remote, branch, opt, cb)](#apidoc.element.gulp-git.push)
- description and source-code
```javascript
push = function (remote, branch, opt, cb) {

  if (!remote) remote = 'origin';
  if (branch === null) {
    branch = '';
  } else if (!branch) {
    branch = 'master';
  }
  if (!cb && typeof opt === 'function') {
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';

  var cmd = 'git push ' + escape([].concat(remote, branch)) + ' ' + opt.args;
  var maxBuffer = opt.maxBuffer || 200 * 1024;

  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb();
  });
}
```
- example usage
```shell
...
  });
});

// Run git push
// remote is the remote repo
// branch is the remote branch to push to
gulp.task('push', function(){
  git.push('origin', 'master', function (err) {
    if (err) throw err;
  });
});

// Run git push with options
// branch is the remote branch to push to
gulp.task('push', function(){
...
```

#### <a name="apidoc.element.gulp-git.removeRemote"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>removeRemote (remote, opt, cb)](#apidoc.element.gulp-git.removeRemote)
- description and source-code
```javascript
removeRemote = function (remote, opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!remote) cb(new Error('gulp-git: remote is required git.removeRemote("origin")'));
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git remote remove ' + opt.args + ' ' + escape([remote]);
  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb();
  });
}
```
- example usage
```shell
...
    if (err) throw err;
  });
});

// Run git remote remove
// remote is the remote repo
gulp.task('removeremote', function(){
  git.removeRemote('origin', function (err) {
    if (err) throw err;
  });
});

// Run git push
// remote is the remote repo
// branch is the remote branch to push to
...
```

#### <a name="apidoc.element.gulp-git.reset"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>reset (commit, opt, cb)](#apidoc.element.gulp-git.reset)
- description and source-code
```javascript
reset = function (commit, opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';
  if (!commit) commit = ' ';

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git reset ' + opt.args + ' ' + escape([commit]);
  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb();
  });

}
```
- example usage
```shell
...
git.merge('branchName', function (err) {
  if (err) throw err;
});
});

// Reset a commit
gulp.task('reset', function(){
git.reset('SHA', function (err) {
  if (err) throw err;
});
});

// Git rm a file or folder
gulp.task('rm', function(){
return gulp.src('./gruntfile.js')
...
```

#### <a name="apidoc.element.gulp-git.revParse"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>revParse (opt, cb)](#apidoc.element.gulp-git.revParse)
- description and source-code
```javascript
revParse = function (opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!opt.args) opt.args = ' '; // it will likely not give you what you want
  if (!opt.cwd) opt.cwd = process.cwd();

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git rev-parse ' + opt.args;
  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (stdout) stdout = stdout.trim(); // Trim trailing cr-lf
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb(err, stdout); // return stdout to the user
  });
}
```
- example usage
```shell
...

'''js
git.reset('HEAD' {args:'--hard'}, function (err) {
  //if (err) ...
});
'''

### git.revParse(opt, cb)
'git rev-parse <options>'

Get details about the repository

'opt': Object (optional) '{args: 'options', cwd: '/cwd/path', quiet: true, maxBuffer: 200 * 1024}'

'cb': function, passed err if any and command stdout
...
```

#### <a name="apidoc.element.gulp-git.rm"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>rm (opt)](#apidoc.element.gulp-git.rm)
- description and source-code
```javascript
rm = function (opt) {
  if (!opt) opt = {};
  if (!opt.args) opt.args = ' ';

  var paths = [];
  var files = [];
  var fileCwd = process.cwd;
  var write = function(file, enc, cb) {
    paths.push(file.path);
    files.push(file);
    fileCwd = file.cwd;
    cb();
  };

  var flush = function(cb) {
    var cwd = opt.cwd || fileCwd;

    var maxBuffer = opt.maxBuffer || 200 * 1024;

    var cmd = 'git rm ' + escape(paths) + ' ' + opt.args;
    var that = this;
    exec(cmd, {cwd: cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
      if (err) cb(err);
      if (!opt.quiet) gutil.log(stdout, stderr);
      files.forEach(that.push.bind(that));
      cb();
    });
  };

  return through.obj(write, flush);
}
```
- example usage
```shell
...
    if (err) throw err;
  });
});

// Git rm a file or folder
gulp.task('rm', function(){
  return gulp.src('./gruntfile.js')
    .pipe(git.rm());
});

gulp.task('addSubmodule', function(){
  git.addSubmodule('https://github.com/stevelacy/git-test', 'git-test', { args: '-b master'});
});

gulp.task('updateSubmodules', function(){
...
```

#### <a name="apidoc.element.gulp-git.stash"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>stash (opt, cb)](#apidoc.element.gulp-git.stash)
- description and source-code
```javascript
stash = function (opt, cb) {

  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }

  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!opt.args) opt.args = 'save --include-untracked "gulp-stash"';
  if (!opt.cwd) opt.cwd = process.cwd();

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git stash ' + opt.args;
  exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    cb(null);
  });

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-git.status"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>status (opt, cb)](#apidoc.element.gulp-git.status)
- description and source-code
```javascript
status = function (opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';
  if (!opt.maxBuffer) opt.maxBuffer = 200 * 1024; // Default buffer value for child_process.exec

  var cmd = 'git status ' + opt.args;
  return exec(cmd, {cwd : opt.cwd, maxBuffer: opt.maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err, stderr);
    if (!opt.quiet) gutil.log(cmd + '\n' + stdout, stderr);
    if (cb) cb(err, stdout);
  });
}
```
- example usage
```shell
...

gulp.task('updateSubmodules', function(){
git.updateSubmodule({ args: '--init' });
});

// Working tree status
gulp.task('status', function(){
git.status({args: '--porcelain'}, function (err, stdout) {
  if (err) throw err;
});
});

// Other actions that do not require a Vinyl
gulp.task('log', function(){
git.exec({args : 'log --follow index.js'}, function (err, stdout) {
...
```

#### <a name="apidoc.element.gulp-git.tag"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>tag (version, message, opt, cb)](#apidoc.element.gulp-git.tag)
- description and source-code
```javascript
tag = function (version, message, opt, cb) {
  if (!cb && typeof opt === 'function') {
    // optional options
    cb = opt;
    opt = {};
  }
  if (!cb && typeof version === 'function') {
    cb = version;
    version = '';
    message = '';
  }
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!message) opt.lightWeight = true; else message = escape([message]);
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var signedarg = opt.signed ? ' -s ' : ' -a ';

  var cmd = 'git tag';
  if (version !== '') {
    if (!opt.lightWeight) {
      cmd += ' ' + signedarg + ' -m ' + message + ' ';
    }
    cmd += opt.args + ' ' + escape([version]);
  }
  var templ = gutil.template(cmd, {file: message});
  return exec(templ, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err) return cb(err);
    if (!opt.quiet && version !== '') gutil.log(stdout, stderr);
    if (version === '') {
      stdout = stdout.split('\n');
    }
    return cb(null, stdout);
  });
}
```
- example usage
```shell
...
git.clone('https://github.com/stevelacy/git-test', {args: './sub/folder'}, function(err) {
  // handle err
});
});

// Tag the repo with a version
gulp.task('tag', function(){
git.tag('v1.1.1', 'Version message', function (err) {
  if (err) throw err;
});
});

// Tag the repo with a version and empty message
gulp.task('tag', function(){
git.tag('v1.1.1', '', function (err) {
...
```

#### <a name="apidoc.element.gulp-git.updateSubmodule"></a>[function <span class="apidocSignatureSpan">gulp-git.</span>updateSubmodule (opt, cb)](#apidoc.element.gulp-git.updateSubmodule)
- description and source-code
```javascript
updateSubmodule = function (opt, cb) {
  if (!cb || typeof cb !== 'function') cb = function () {};
  if (!opt) opt = {};
  if (!opt.cwd) opt.cwd = process.cwd();
  if (!opt.args) opt.args = ' ';

  var maxBuffer = opt.maxBuffer || 200 * 1024;

  var cmd = 'git submodule update ' + opt.args;
  return exec(cmd, {cwd: opt.cwd, maxBuffer: maxBuffer}, function(err, stdout, stderr) {
    if (err && cb) cb(err);
    if (!opt.quiet) gutil.log(stdout, stderr);
    if (cb) cb();
  });
}
```
- example usage
```shell
...
});

gulp.task('addSubmodule', function(){
git.addSubmodule('https://github.com/stevelacy/git-test', 'git-test', { args: '-b master'});
});

gulp.task('updateSubmodules', function(){
git.updateSubmodule({ args: '--init' });
});

// Working tree status
gulp.task('status', function(){
git.status({args: '--porcelain'}, function (err, stdout) {
  if (err) throw err;
});
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
