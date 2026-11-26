# nongying-models

弄影（Nongying）的 AI 模型权重分发仓——应用内「设置 > AI 模型」下载通道的主源。

## face-landmarker-v1（MediaPipe Face Landmarker，tf2onnx 自转）

| 文件 | 体积 (B) | sha256 |
| --- | --- | --- |
| `face_detector.onnx` | 4,184,447 | `b4f5da0b136cbe799d20929095c673f0ee4f5b77c529f3c40eb5a7f6aafd04c6` |
| `face_landmarks_detector.onnx` | 4,920,998 | `685aa345d307a161ac26a2055c1ed256fee8be501d9a0305ab11b402f5d25e0a` |
| `face_blendshapes.onnx` | 1,884,379 | `01a3aff8339a59b947a3eade8b2d3cdaf4fdb3b9dd5573441dfefed363d2b1fd` |

- **上游**：MediaPipe Face Landmarker `face_landmarker.task`（float16/latest 档，3,758,596 B，sha256 `64184e229b263107bc2b804c6625db1341ff2bb731874b0bcc2fe6544e0bc9ff`）
- **来源**：`storage.googleapis.com/mediapipe-models/face_landmarker/face_landmarker/float16/latest/face_landmarker.task`
- **许可**：Apache-2.0（上游 [google-ai-edge/mediapipe](https://github.com/google-ai-edge/mediapipe) 仓库 LICENSE）
- **本仓变更**：仅格式转换（官方 tf2onnx 自转，opset 15），无权重改动；转换/对拍读数见弄影仓 `docs/AI-MODELS.md`
- **消费**：按上述落盘名放进用户模型目录即可被应用探测；应用内下载会做 sha256 校验
