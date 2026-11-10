# compile-llama.cpp

Este repositório reúne arquivos e instruções de compilação do [llama.cpp](https://github.com/ggml-org/llama.cpp), com o objetivo de permitir a execução de modelos usando **CPU** ou **GPU**.

## Compilar para CPU

Com um compilador C/C++ e o CMake instalados:

```bash
git clone --recursive https://github.com/ggml-org/llama.cpp.git
cd llama.cpp
cmake -B build -DGGML_CUDA=OFF
cmake --build build --config Release
```

## Compilar para GPU NVIDIA (CUDA)

Com os drivers e o CUDA Toolkit compatíveis instalados:

```bash
git clone --recursive https://github.com/ggml-org/llama.cpp.git
cd llama.cpp
cmake -B build -DGGML_CUDA=ON
cmake --build build --config Release
```

A opção `GGML_CUDA` habilita o backend CUDA. Outros backends de GPU podem exigir opções e dependências diferentes, conforme o hardware e o sistema operacional.

## Objetivo

A ideia é documentar e organizar configurações e scripts que facilitem a compilação do llama.cpp em diferentes ambientes. As instruções devem ser ajustadas conforme a plataforma, o compilador e o backend de GPU disponíveis.
