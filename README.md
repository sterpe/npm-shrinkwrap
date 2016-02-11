# npm-shrinkwrap bug

## Steps to reproduce

	node --version # 4.2.4
	npm --version # 2.14.12
	npm i # notice that there are no warnings.
	npm shrinkwrap --dev
	rm -rf node_modules
	npm i # now there is a warning about browserify being auto installed as a peerDependency

## Expected

If a dependency or devDependency is explicitly listed in the `package.json` it shouldn't
become a peerDependency from the perspective of a shrinkwrap install.

