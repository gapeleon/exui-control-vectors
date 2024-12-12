
<p  align="center">

# ExUI with Control Vectors

A fork of [ExUI](https://github.com/turboderp/exui) adding support for creative writing control vectors in ExLlamaV2.

### Overview of Features

All original ExUI features plus:

- Support for creative writing control vectors
- Multiple vector combinations
- Dynamic weight adjustment
- Visual control vector configuration

### Control Vectors Support

This fork adds support for [jukofyork's creative writing control vectors](https://huggingface.co/jukofyork/creative-writing-control-vectors-v3.0), allowing dynamic control over the model's writing style.

#### Directory Structure

Your control vectors should be placed in a "-vectors" directory next to your model:
```

models/

├── Your-Model-Name/

│ └── model files...

└── Your-Model-Name-vectors/

│ └── vector-name__debias.gguf

│ └──  vector-name__direction1.gguf

│ └──  vector-name__direction2.gguf

│ └──  ...

```

#### Using Control Vectors


1. Add vectors to your model's "-vectors" directory

2. In the model settings page, enable "Control Vectors"

3. Add vector configurations in the format: `vector:direction:weight`

- Example: `humility_vs_narcissism:narcissism:1.0`

4. Multiple vectors can be combined with different weights

- Example: `humility_vs_narcissism:narcissism:1.4,empathy_vs_sociopathy:sociopathy:1.0`


Positive weights enhance the named direction, negative weights push toward the opposite.

  

### Installation

1. Clone this repository:

```bash
git  clone  https://github.com/gapeleon/exui-controlvectors
cd  exui-control
pip  install  -r  requirements.txt
```

2. Run the web server:

```bash
python  server.py
```
Your browser should automatically open on the default IP/port. Config and sessions are stored in `~/exui` by default.

### Credits

- Original [ExUI](https://github.com/turboderp/exui) by turboderp

- [ExLlamaV2](https://github.com/turboderp/exllamav2/) by turboderp

- Control vector wrapper for exllamav2 by [llmixer/ExllamaV2-Control-Vectors](https://huggingface.co/llmixer/ExllamaV2-Control-Vectors)

- Creative writing control vectors by [jukofyork](https://huggingface.co/jukofyork/creative-writing-control-vectors-v3.0)

### Screenshots

[TODO add screenshots showing the control vector UI and example outputs]

