### magicpython
---
https://github.com/MagicStack/MagicPython

```makefile
.PHONY: all ci-test test release devenv publish

all: devenv release

ci-test: release
#
  ./node_modules/.bin/syntaxdev test --tests test/**/*.py --syntax grammars/src/MagicPython.syntax.yaml
  ./node_modules/.bin/syntaxdev test --tests test/**/*.re --syntax grammrs/src/MagicRegExp.syntax.yaml
#
  @if [ \
    `cat package.json | grep -e''` \
    != \
    `` \
  ] ; \
    then echo "" && exit 1 ; fi
    
test: ci-test
  atom -t test/atom-spec
  
devenv:
  npm install --dev
  
release:
  ./node_modules/.bin/syntaxdev build-plist --in grammars/src/MagicPython.syntax.yaml --out grammars/MagicPython.tmLanguage
  ./node_modules/.bin/
  
  ./node_modules/.bin
  ./node_modules/.bin
  
  ./node_modules/.bin
  
  ./node_module/.bin
  ./node_module/.bin
  
publish: test
  apm publish patch
  rm -rf ./node_modules/syntaxdev
  vsce publish
```

```
```

```
```

