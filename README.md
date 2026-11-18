# speech-models

Copies of two converted versions of OpenAI's **Whisper large-v3-turbo** speech model, kept here so a speech tool can download them
from GitHub. Every file is byte for byte the file from its source; nothing is changed.

The files are in the release **`whisper-large-v3-turbo-1`** (it is never changed; a new model gets a new release).

| release file | from | size (bytes) | SHA-256 |
|---|---|---|---|
| `fw-model.bin` | `model.bin` | 1617884929 | `e76620f83d5f5b69efd3d87e3dc180c1bd21df9fbebacfd4335e5e1efcc018da` |
| `fw-config.json` | `config.json` | 2263 | `b0253ea6c0d3bea6b1e19e91a02acfd3b53f4467362efcb5a3e6b16c9b3a9b7e` |
| `fw-preprocessor_config.json` | `preprocessor_config.json` | 340 | `7ccc62c6f2765af1f3b46c00c9b5894426835a05021c8b9c01eecb6dfb542711` |
| `fw-tokenizer.json` | `tokenizer.json` | 2710337 | `297b13372ac43916285644fb9687add3cc62ee2a1adb60da3dc25cc94c1871fd` |
| `fw-vocabulary.json` | `vocabulary.json` | 1068114 | `c69260f2ab26d659b7c398f9a2b2b48ed0df16c3b47d7326782fd9cba71690c1` |
| `mlx-weights.safetensors` | `weights.safetensors` | 1613977612 | `951ed3fc1203e6a62467abb2144a96ce7eafca8fa77e3704fdb8635ff3e7f8a6` |
| `mlx-config.json` | `config.json` | 268 | `b34fc29e4e11e0a25e812775dd67f4dd16fc2c8eb43d28ae25ff7d660ecb6379` |

`SHA256SUMS` in the release lists the same fingerprints.

## Sources

- `fw-*`: the CTranslate2 conversion used by [faster-whisper](https://github.com/SYSTRAN/faster-whisper) for `large-v3-turbo`:
  [dropbox-dash/faster-whisper-large-v3-turbo](https://huggingface.co/dropbox-dash/faster-whisper-large-v3-turbo) (formerly
  `mobiuslabsgmbh/faster-whisper-large-v3-turbo`), commit `0a363e9161cbc7ed1431c9597a8ceaf0c4f78fcf`. Licence: MIT. Its model card is
  in `model-cards/`.
- `mlx-*`: the MLX conversion used by [mlx-whisper](https://github.com/ml-explore/mlx-examples):
  [mlx-community/whisper-large-v3-turbo](https://huggingface.co/mlx-community/whisper-large-v3-turbo), commit
  `a4aaeec0636e6fef84abdcbe3544cb2bf7e9f6fb`. Its model card is in `model-cards/`.
- Both are conversions of [openai/whisper-large-v3-turbo](https://huggingface.co/openai/whisper-large-v3-turbo), released by OpenAI
  under the MIT licence: see `LICENSE` (OpenAI's text).
