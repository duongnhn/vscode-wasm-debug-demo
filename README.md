# WASM DEBUGGING EXPERIENCE IN VSCODE USING vscode-js-debug EXTENSION

# Prequisites
Emscripten: https://emscripten.org/docs/getting_started/downloads.html
Launch chrome at http://localhost:4000
Load vscode-js-debug extension https://github.com/microsoft/vscode-js-debug 

# Debug without source map
emcc test.c -O2 -s SIDE_MODULE=1 -o test.wasm

# Debug with source map
emcc test.c -O3 -s SIDE_MODULE=1 -g4 --source-map-base http://localhost:4000/ -o test.wasm
