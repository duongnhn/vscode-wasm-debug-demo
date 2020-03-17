# WASM DEBUGGING EXPERIENCE IN VSCODE USING vscode-js-debug EXTENSION

# Prequisites
1. Emscripten: https://emscripten.org/docs/getting_started/downloads.html
2. Server this repo at http://localhost:4000
3. Load vscode-js-debug extension https://github.com/microsoft/vscode-js-debug 

# Debug without source map
emcc test.c -O2 -s SIDE_MODULE=1 -o test.wasm

# Debug with source map
emcc test.c -O3 -s SIDE_MODULE=1 -g4 --source-map-base http://localhost:4000/ -o test.wasm
