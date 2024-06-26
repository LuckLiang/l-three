# 背景

随着数字孪生技术的快速发展和广泛应用，Web 前端开发的角色正在扩展，不仅局限于传统的平面界面设计与交互实现，更承载了日益增多的三维场景展示任务。尤其是在工业制造、智慧城市、建筑设计、虚拟现实等领域，数字孪生技术通过构建与物理世界实时对应、高度仿真的虚拟模型，为决策分析、模拟预测、远程监控等提供了强大支持。

# 特性

该插件基于强大的 WebGL 渲染库 Three.js 进行二次开发，以便快速搭建功能相对简单但又不失专业性的数字孪生场景。

# 场景说明

- 初始化相机为 PerspectiveCamera
- 控制器为 OrbitControls
- 灯光为 AmbientLight*1、DirectionalLight*1、HemisphereLight\*1
- 渲染器默认为 WebGLRenderer

# 已完成功能

- 支持 dom 面板插入
- 模型发光
- 模型拾取
- 支持第一/三人称控制器
- 场景切换
- 天气效果，如雨雪雾等天气

# 安装

```
npm install qs-three
```

# 使用

## VUE 中使用

```
// 此示例是Vue3版本,Vue2 同理
import QSTHREE from "qs-three";

onMounted(() => {
  const QsThree = new QSTHREE.QsThree(content3d.value, {
    modelUrl: "http://localhost:8090/model/factory/factory.gltf",
    isGUP: true,
  });
  QsThree.animate();
});
```

## VUE3 演示项目地址

```
https://gitee.com/klus-liang/qs-three.-vue3.-vite.git
```
