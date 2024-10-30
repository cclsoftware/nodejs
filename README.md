# Node.js headers for CCL-based addons

This repository contains a subset of the original Node.js repository found at https://github.com/nodejs/node for the development of CCL-based addons.

### Version

The content of this repository is copied from the original repository of Node.js:

```
Version 2.18.0 'Iron' (LTS)
Branch: v20.x
Tag: v20.18.0
Commit: 7eebd17fa2c1e48e4534f3a69560388fab2f2c07
```

Execute the following steps to update this repository to a newer version of Node.js:

1. Clone the Node.js repository to a local folder.
2. Copy the files `node_api.h`, `node_api_types.h`, `js_native_api.h` and `js_native_api_types.h` from the Node.js `/src` directory to the `/include` directory in this repository.
3. Copy the file `uv.h` from the Node.js `/deps/uv/include` directory in the `/ìnclude` directory and update the files in `/include/uv` of this repo from `/deps/uv/include/uv` in the Node.js directory.
4. The file `node.lib` for Windows must be compiled locally. This is done by issuing the command `./vcbuild openssl-no-asm` in the local Node.js repository. The resulting file `/out/Release/node.lib` must be copied to the `/lib/windows` directory of this repository. Further details on building Node.js on Windows and the necessary prerequisites can be found at https://github.com/nodejs/node/blob/main/BUILDING.md#windows.

