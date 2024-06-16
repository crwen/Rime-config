My [Rime](https://github.com/rime/squirrel) config.

You can set global default settings in `default.yaml`

```yaml
# 方案列表
schema_list:
  # 可以直接删除或注释不需要的方案，对应的 *.schema.yaml 方案文件也可以直接删除
  # 除了 t9，它依赖于 rime_ice，用九宫格别删 rime_ice.schema.yaml
  - schema: rime_ice # 雾凇拼音（全拼）
  # - schema: t9 # 九宫格（仓输入法）
  # - schema: double_pinyin # 自然码双拼
  # - schema: double_pinyin_abc # 智能 ABC 双拼
  # - schema: double_pinyin_mspy # 微软双拼
  # - schema: double_pinyin_sogou # 搜狗双拼
  # - schema: double_pinyin_flypy # 小鹤双拼
  # - schema: double_pinyin_ziguang # 紫光双拼
```

You can also set your key bindings here

```yaml
# 快捷键
key_binder:
  bindings:
    # vim_editing:
    - { when: composing, accept: Control+k, send: Left }
    - { when: composing, accept: Control+j, send: Right }
    - { when: composing, accept: Control+p, send: Up }
    - { when: composing, accept: Control+n, send: Down }

    - { when: composing, accept: Control+h, send: BackSpace }
    - { when: composing, accept: Control+w, send: Shift+BackSpace }

    - { when: composing, accept: Control+a, send: Home }
    - { when: composing, accept: Control+e, send: End }
```

In `squirrel.custom.yaml`, you can configure style. Settings in `squireel.yaml` will be overwriten. You can see [wiki](https://github.com/rime/home/wiki/CustomizationGuide#%E5%AE%9A%E8%A3%BD%E6%8C%87%E5%8D%97) or [Rime配置](https://dvel.me/posts/rime-ice/#%E4%BB%A5-patch-%E7%9A%84%E6%96%B9%E5%BC%8F%E6%89%93%E8%A1%A5%E4%B8%81) to see how to patch. (Thanks for [Lucius-Wang/rime-config](https://github.com/Lucius-Wang/rime-config)'s presets).

You can also configure your default input method here:

```yaml
patch:
  # 以下软件默认英文模式
  app_options:
    com.microsoft.VSCode:
      ascii_mode: true
    com.jetbrains.intellij:
      ascii_mode: true
    com.apple.Terminal:
      ascii_mode: true
    com.googlecode.iterm2:
      ascii_mode: true
    com.github.wez.wezterm:
      ascii_mode: true
    org.alacritty:
      ascii_mode: true
```

In `custom_pharse.txt`, you can add your personal words.

Thanks for

- [Rime](https://github.com/rime/squirrel)
- [iDvel/rime-ice](https://github.com/iDvel/rime-ice)
- [Lucius-Wang/rime-config](https://github.com/Lucius-Wang/rime-config)
