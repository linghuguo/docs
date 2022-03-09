---
sidebar_position: 1
---
# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [protos/riaid.proto](#protos/riaid.proto)
    - [ADActionModel](#riaid.ADActionModel)
    - [ADAnimationModel](#riaid.ADAnimationModel)
    - [ADBrowserLifeCycleModel](#riaid.ADBrowserLifeCycleModel)
    - [ADCancelTimerActionModel](#riaid.ADCancelTimerActionModel)
    - [ADConditionChangeActionModel](#riaid.ADConditionChangeActionModel)
    - [ADConditionLogicModel](#riaid.ADConditionLogicModel)
    - [ADConditionModel](#riaid.ADConditionModel)
    - [ADConditionTriggerModel](#riaid.ADConditionTriggerModel)
    - [ADConversionActionModel](#riaid.ADConversionActionModel)
    - [ADConversionActionModel.BundleEntry](#riaid.ADConversionActionModel.BundleEntry)
    - [ADCustomActionModel](#riaid.ADCustomActionModel)
    - [ADCustomActionModel.ParametersEntry](#riaid.ADCustomActionModel.ParametersEntry)
    - [ADFunctionModel](#riaid.ADFunctionModel)
    - [ADGeneralTriggerModel](#riaid.ADGeneralTriggerModel)
    - [ADHeartBeatTriggerModel](#riaid.ADHeartBeatTriggerModel)
    - [ADInSceneAnimationTransitionModel](#riaid.ADInSceneAnimationTransitionModel)
    - [ADLogicUnitModel](#riaid.ADLogicUnitModel)
    - [ADLottieTransitionModel](#riaid.ADLottieTransitionModel)
    - [ADReadAttributeFunctionModel](#riaid.ADReadAttributeFunctionModel)
    - [ADRenderContentTransitionModel](#riaid.ADRenderContentTransitionModel)
    - [ADRenderWrapModel](#riaid.ADRenderWrapModel)
    - [ADSceneLifeCycleModel](#riaid.ADSceneLifeCycleModel)
    - [ADSceneModel](#riaid.ADSceneModel)
    - [ADSceneRelationModel](#riaid.ADSceneRelationModel)
    - [ADSceneShareTransitionModel](#riaid.ADSceneShareTransitionModel)
    - [ADStepActionModel](#riaid.ADStepActionModel)
    - [ADTemplateTransitionModel](#riaid.ADTemplateTransitionModel)
    - [ADTimeoutTriggerModel](#riaid.ADTimeoutTriggerModel)
    - [ADTrackActionModel](#riaid.ADTrackActionModel)
    - [ADTrackActionModel.ParametersEntry](#riaid.ADTrackActionModel.ParametersEntry)
    - [ADTransitionActionModel](#riaid.ADTransitionActionModel)
    - [ADTransitionModel](#riaid.ADTransitionModel)
    - [ADTranslationTransitionModel](#riaid.ADTranslationTransitionModel)
    - [ADTriggerActionModel](#riaid.ADTriggerActionModel)
    - [ADTriggerModel](#riaid.ADTriggerModel)
    - [ADUrlActionModel](#riaid.ADUrlActionModel)
    - [ADUrlActionModel.BundleEntry](#riaid.ADUrlActionModel.BundleEntry)
    - [ADVariableChangeActionModel](#riaid.ADVariableChangeActionModel)
    - [ADVideoActionModel](#riaid.ADVideoActionModel)
    - [ADVideoDurationTimeoutTriggerModel](#riaid.ADVideoDurationTimeoutTriggerModel)
    - [ADVisibilityTransitionModel](#riaid.ADVisibilityTransitionModel)
    - [Attributes](#riaid.Attributes)
    - [BasicVariable](#riaid.BasicVariable)
    - [BasicVariableValue](#riaid.BasicVariableValue)
    - [BasicVariableValue.Value](#riaid.BasicVariableValue.Value)
    - [BoolValue](#riaid.BoolValue)
    - [ButtonAttributes](#riaid.ButtonAttributes)
    - [ButtonAttributes.HighlightState](#riaid.ButtonAttributes.HighlightState)
    - [CommonAttributes](#riaid.CommonAttributes)
    - [CornerRadius](#riaid.CornerRadius)
    - [FloatValue](#riaid.FloatValue)
    - [Gradient](#riaid.Gradient)
    - [Handler](#riaid.Handler)
    - [ImageAttributes](#riaid.ImageAttributes)
    - [Int32Value](#riaid.Int32Value)
    - [Layout](#riaid.Layout)
    - [Layout.Edge](#riaid.Layout.Edge)
    - [LottieAttributes](#riaid.LottieAttributes)
    - [LottieAttributes.ReplaceText](#riaid.LottieAttributes.ReplaceText)
    - [Node](#riaid.Node)
    - [Responder](#riaid.Responder)
    - [RiaidModel](#riaid.RiaidModel)
    - [ScrollAttributes](#riaid.ScrollAttributes)
    - [Shadow](#riaid.Shadow)
    - [Stroke](#riaid.Stroke)
    - [SystemKeyEnum](#riaid.SystemKeyEnum)
    - [TextAttributes](#riaid.TextAttributes)
    - [TextAttributes.Align](#riaid.TextAttributes.Align)
    - [TextAttributes.RichText](#riaid.TextAttributes.RichText)
    - [VideoAttributes](#riaid.VideoAttributes)
    - [VideoHandler](#riaid.VideoHandler)
  
    - [ADAnimationModel.ViewPropertyType](#riaid.ADAnimationModel.ViewPropertyType)
    - [ADSceneRelationModel.SceneEdge](#riaid.ADSceneRelationModel.SceneEdge)
    - [ADTemplateTransitionModel.TemplateType](#riaid.ADTemplateTransitionModel.TemplateType)
    - [ADVideoActionModel.VideoControlType](#riaid.ADVideoActionModel.VideoControlType)
    - [Attributes.AttributeType](#riaid.Attributes.AttributeType)
    - [BasicVariableValue.Type](#riaid.BasicVariableValue.Type)
    - [CommonAttributes.ShapeType](#riaid.CommonAttributes.ShapeType)
    - [CompareOperator](#riaid.CompareOperator)
    - [Gradient.GradientAngle](#riaid.Gradient.GradientAngle)
    - [Gradient.GradientType](#riaid.Gradient.GradientType)
    - [ImageAttributes.ScaleType](#riaid.ImageAttributes.ScaleType)
    - [LogicOperator](#riaid.LogicOperator)
    - [LottieAttributes.RepeatMode](#riaid.LottieAttributes.RepeatMode)
    - [Node.ClassType](#riaid.Node.ClassType)
    - [SystemKeyEnum.SystemKeys](#riaid.SystemKeyEnum.SystemKeys)
    - [TextAttributes.Align.Horizontal](#riaid.TextAttributes.Align.Horizontal)
    - [TextAttributes.Align.Vertical](#riaid.TextAttributes.Align.Vertical)
    - [TextAttributes.Ellipsize](#riaid.TextAttributes.Ellipsize)
    - [TextAttributes.LineMode](#riaid.TextAttributes.LineMode)
  
- [Scalar Value Types](#scalar-value-types)



<a name="protos/riaid.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## protos/riaid.proto



<a name="riaid.ADActionModel"></a>

### ADActionModel
所有Action的封装类
注意，这里面的成员只能有一个，因为客户端使用的MessageNano，因为解析原因，暂不使用oneof


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| transition | [ADTransitionActionModel](#riaid.ADTransitionActionModel) |  | 所有Transition的行为，通常用于场景的转场或场景内动画 |
| track | [ADTrackActionModel](#riaid.ADTrackActionModel) |  | 埋点的Action，由上层解析和发送 |
| video | [ADVideoActionModel](#riaid.ADVideoActionModel) |  | 视频播放控制的Action |
| url | [ADUrlActionModel](#riaid.ADUrlActionModel) |  | url的Action，可以是直接跳转落地页，也可以转化跳转 |
| condition_change | [ADConditionChangeActionModel](#riaid.ADConditionChangeActionModel) |  | 条件变化Action |
| cancel_timer | [ADCancelTimerActionModel](#riaid.ADCancelTimerActionModel) |  | 取消一个正在进行中的timerTrigger |
| custom | [ADCustomActionModel](#riaid.ADCustomActionModel) |  | 自定义的行为，用于透传的 |
| trigger | [ADTriggerActionModel](#riaid.ADTriggerActionModel) |  | 触发一个Trigger |
| conversion | [ADConversionActionModel](#riaid.ADConversionActionModel) |  | 转化跳转的action |
| step | [ADStepActionModel](#riaid.ADStepActionModel) |  | 分步执行的action，处理一个变量 |
| variable_change | [ADVariableChangeActionModel](#riaid.ADVariableChangeActionModel) |  | 变量变化action |






<a name="riaid.ADAnimationModel"></a>

### ADAnimationModel
广告的动画定义，用来描述了属性动画的一些配置 6


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| property_type | [ADAnimationModel.ViewPropertyType](#riaid.ADAnimationModel.ViewPropertyType) |  |  |
| duration | [int64](#int64) |  |  |
| repeat_count | [int32](#int32) |  | 如果等于-1则是重复执行 |
| values | [float](#float) | repeated | 如果是宽或高的值，则-1是认为渲染好的宽高 |






<a name="riaid.ADBrowserLifeCycleModel"></a>

### ADBrowserLifeCycleModel
ADBrowser生命周期模型


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| appear_trigger_keys | [int32](#int32) | repeated | RIAID所在的页面推入或从后台切换到前台。对齐Android的onResume和iOS的onDidAppear以及从后台切换到前台 |
| disappear_trigger_keys | [int32](#int32) | repeated | RIAID所在的页面压栈或从前台切换到后台。对齐Android的onPause和iOS的onDidDisappear以及从前台切换到后台 |
| load_trigger_keys | [int32](#int32) | repeated | 加载广告，例如广告滑入时会调用。一般我们会在广告进入时，去触发广告场景开始展示。 |
| unload_trigger_keys | [int32](#int32) | repeated | 卸载广告，例如广告滑出时调用。 |






<a name="riaid.ADCancelTimerActionModel"></a>

### ADCancelTimerActionModel
作用: 取消一个正在进行中的时间控制器
概念解释：
1.时间触发器: RIAID 协议中定义的用于触发时间控制的概念。目前有两种，分别为:定时操作(ADTimeoutTriggerModel),心跳操作
(ADHeartBeatTriggerModel)。
2.时间控制器: 引擎实现的时候，对于时间触发器的一个实例化，负责进行具体的时间控制行为。
3.时间控制器与时间触发器，维持1:1的关系。在同一个时刻，一个时间触发器只能实例化一个时间控制器。
具体功能描述: 通过trigger_key获得对应的时间触发器，取消该时间触发器对应的时间控制器。
注意: 这里取消的是时间控制器，而非时间触发器。


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| trigger_key | [int32](#int32) |  | 一个ADTimeoutTriggerModel的key或者是一个ADHeartBeatTriggerModel的key |






<a name="riaid.ADConditionChangeActionModel"></a>

### ADConditionChangeActionModel
条件变化Action


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| condition | [ADConditionModel](#riaid.ADConditionModel) |  | 条件模型 |






<a name="riaid.ADConditionLogicModel"></a>

### ADConditionLogicModel
如果内部logic，units组成的条件符合，执行action_models


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| operator | [LogicOperator](#riaid.LogicOperator) |  |  |
| units | [ADLogicUnitModel](#riaid.ADLogicUnitModel) | repeated |  |
| actions | [ADActionModel](#riaid.ADActionModel) | repeated | Action集合 |






<a name="riaid.ADConditionModel"></a>

### ADConditionModel
用以记录Browser当前的条件，概念类似于环境变量


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| condition_name | [string](#string) |  | 条件的名字 |
| condition_value | [string](#string) |  | 条件对应的值 |






<a name="riaid.ADConditionTriggerModel"></a>

### ADConditionTriggerModel



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [int32](#int32) |  | condition trigger key |
| logics | [ADConditionLogicModel](#riaid.ADConditionLogicModel) | repeated | ADConditionLogicModel 同一时间，数组内应当有且仅有一个ADConditionLogicModel是符合执行条件的 |
| debug_info | [string](#string) |  | 用来说明该触发器是做什么用的，简单描述。 |






<a name="riaid.ADConversionActionModel"></a>

### ADConversionActionModel
有转化的跳转url，这个行为透传给上层处理


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| url | [string](#string) |  | 要跳转的url |
| deep_link | [string](#string) |  | 要跳转的deep_link，可以是跳转应用 |
| bundle | [ADConversionActionModel.BundleEntry](#riaid.ADConversionActionModel.BundleEntry) | repeated | 可能要透传的打包数据 |






<a name="riaid.ADConversionActionModel.BundleEntry"></a>

### ADConversionActionModel.BundleEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [string](#string) |  |  |






<a name="riaid.ADCustomActionModel"></a>

### ADCustomActionModel
自定义的行为，用于透传的


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parameters | [ADCustomActionModel.ParametersEntry](#riaid.ADCustomActionModel.ParametersEntry) | repeated |  |






<a name="riaid.ADCustomActionModel.ParametersEntry"></a>

### ADCustomActionModel.ParametersEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [string](#string) |  |  |






<a name="riaid.ADFunctionModel"></a>

### ADFunctionModel
有返回值的内置函数
目前仅用于埋点中存在#{in_fun_key}时，需要调用这个内置函数，并将其返回值替换掉#{in_fun_key}
只能有一个function


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| read_attribute | [ADReadAttributeFunctionModel](#riaid.ADReadAttributeFunctionModel) |  |  |






<a name="riaid.ADGeneralTriggerModel"></a>

### ADGeneralTriggerModel
普通触发器


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [int32](#int32) |  | 触发器的key |
| actions | [ADActionModel](#riaid.ADActionModel) | repeated | Action集合 |
| debug_info | [string](#string) |  | 用来说明该触发器是做什么用的，简单描述。 |






<a name="riaid.ADHeartBeatTriggerModel"></a>

### ADHeartBeatTriggerModel
心跳触发器，例如：每隔3秒，触发操作


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [int32](#int32) |  | 触发器的key |
| interval | [int64](#int64) |  | 触发间隔，单位毫秒，例：time=1000，每隔1秒，触发一次 |
| count | [int32](#int32) |  | 需要执行次数 |
| actions | [ADActionModel](#riaid.ADActionModel) | repeated | Action集合 |
| debug_info | [string](#string) |  | 用来说明该触发器是做什么用的，简单描述。 |






<a name="riaid.ADInSceneAnimationTransitionModel"></a>

### ADInSceneAnimationTransitionModel
场景内的转场动画


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| view_key | [int32](#int32) |  |  |
| animation | [ADAnimationModel](#riaid.ADAnimationModel) |  |  |






<a name="riaid.ADLogicUnitModel"></a>

### ADLogicUnitModel
逻辑单元，用以比较condition或variable是否符合逻辑
condition和variable只能一个有值


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| condition | [ADConditionModel](#riaid.ADConditionModel) |  |  |
| compare | [CompareOperator](#riaid.CompareOperator) |  | 此compare比较的是condition或variable与全局存储的condition或variable的值 |
| variable | [BasicVariable](#riaid.BasicVariable) |  |  |






<a name="riaid.ADLottieTransitionModel"></a>

### ADLottieTransitionModel



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| scene_key | [int32](#int32) |  | 支持lottie的具体场景 |
| lottie_type | [string](#string) |  | lottie的类型，目前支持progress |
| view_keys | [int32](#int32) | repeated | 可以为空，如果为空，则是该场景下支持lottie的所有组件改变状态 |
| max_progress | [int64](#int64) |  | 最大的进度，如倒计时6s，则maxProgress为6000 |
| interval | [int64](#int64) |  | lottie状态更新间隔，如倒计时6s，每隔100ms触发一次状态，则interval为100 |






<a name="riaid.ADReadAttributeFunctionModel"></a>

### ADReadAttributeFunctionModel
读取Node属性的内置函数


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [int32](#int32) |  | 内置函数的唯一地址 |
| view_key | [int32](#int32) |  | Node的id |
| attribute_type | [Attributes.AttributeType](#riaid.Attributes.AttributeType) |  | 属性名 |






<a name="riaid.ADRenderContentTransitionModel"></a>

### ADRenderContentTransitionModel
场景内的特定Transition，用于更新render的内容


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| view_key | [int32](#int32) |  | 要更新的render其中的view |
| render_attributes | [Attributes](#riaid.Attributes) |  | 要更新的属性 |






<a name="riaid.ADRenderWrapModel"></a>

### ADRenderWrapModel
渲染对象的包裹


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| render_data | [Node](#riaid.Node) |  | 通过构建的Render对象，获取视图 |






<a name="riaid.ADSceneLifeCycleModel"></a>

### ADSceneLifeCycleModel
Scene生命周期模型


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| appear_trigger_keys | [int32](#int32) | repeated | Scene展示时需要触发的TriggerKeys，hidden=false |
| disappear_trigger_keys | [int32](#int32) | repeated | Scene消失时需要触发的TriggerKeys，hidden=true |






<a name="riaid.ADSceneModel"></a>

### ADSceneModel
场景的model，用对场景的描述


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [int32](#int32) |  |  |
| render | [ADRenderWrapModel](#riaid.ADRenderWrapModel) |  |  |
| debug_info | [string](#string) |  | 用来说明该场景是做什么用的，简单描述。 |
| life_cycle | [ADSceneLifeCycleModel](#riaid.ADSceneLifeCycleModel) |  | 场景生命周期 |






<a name="riaid.ADSceneRelationModel"></a>

### ADSceneRelationModel
声明本场景与目标的关系
具体用法：
以target为基准，固定source的位置
source的sourceEdge在target的targetEdge
source的sourceEdge相对于target的targetEdge的距离为distance
注意：
- sourceEdge与targetEdge必须成对存在，方向也成对存在，横向有start和end，纵向有top和bottom，如sourceEdge声明为横向，则targetEdge
也必须为横向。
- ADSceneRelation通常是组合使用，source两个方向都应该有约束，若其中一个方向没有约束，则认为该方向相对于Canvas居中。
- 单一坐标轴上只需要描述一个边缘即可。
- 不能重复描述一个元素同一个边缘的约束关系。
- 同一个钢性元素，需要同时描述纵向和横向的边缘。
- 若target为canvas，仅支持同一个方向的约束，例：支持sourceEdge=start，targetEdge=start，不支持sourceEdge=start
，targetEdge=end。


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| source_key | [int32](#int32) |  | 场景的key |
| target_key | [int32](#int32) |  | 场景的key,特殊说明Canvas |
| distance | [float](#float) |  | 设计稿的逻辑像素 |
| source_edge | [ADSceneRelationModel.SceneEdge](#riaid.ADSceneRelationModel.SceneEdge) |  | 本场景的边 |
| target_edge | [ADSceneRelationModel.SceneEdge](#riaid.ADSceneRelationModel.SceneEdge) |  | 目标场景的边 |






<a name="riaid.ADSceneShareTransitionModel"></a>

### ADSceneShareTransitionModel
场景与场景的共享元素转场过渡动画
给到两个scene，两个scene若复用view，则其viewKey相同。如复用的view为ActionButton，SceneA的ActionButton作为起始态，SceneB
的ActionButton作为最终态，然后执行动画


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| start_scene_key | [int32](#int32) |  | Transition对应的场景，作为起始态 |
| end_scene_key | [int32](#int32) |  | Transition对应的目标场景，作为最终态 |
| duration | [int64](#int64) |  | ms，起始态到最终态的动画时间。 |






<a name="riaid.ADStepActionModel"></a>

### ADStepActionModel
ADStepActionModel是一个分步的行为，分步行为需要对变量操作value+step，
变量操作之后会对这个变量做内置函数的处理，最后触发触发器


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| max | [int32](#int32) |  | 变量操作不能超过这个最大值，如果超过了自动停止 |
| min | [int32](#int32) |  | 变量操作不能小于这个最小值，如果小于了自动停止 |
| step | [int32](#int32) |  | 间隔，可正可负 |
| variable_key | [int32](#int32) |  | 变量的地址，这个变量的Type要求是INTEGER |
| trigger_keys | [int32](#int32) | repeated | 每步操作完变量后要执行的触发器 |






<a name="riaid.ADTemplateTransitionModel"></a>

### ADTemplateTransitionModel
场景模板转场描述


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| scene_key | [int32](#int32) |  |  |
| duration | [int64](#int64) |  |  |
| template | [ADTemplateTransitionModel.TemplateType](#riaid.ADTemplateTransitionModel.TemplateType) |  |  |






<a name="riaid.ADTimeoutTriggerModel"></a>

### ADTimeoutTriggerModel
定时触发器，例如：3秒后触发操作


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [int32](#int32) |  | 触发器的key |
| interval | [int64](#int64) |  | 触发时机，单位毫秒，例：time=1000，则为1s后触发 |
| actions | [ADActionModel](#riaid.ADActionModel) | repeated | Action集合 |
| debug_info | [string](#string) |  | 用来说明该触发器是做什么用的，简单描述。 |






<a name="riaid.ADTrackActionModel"></a>

### ADTrackActionModel
埋点的Action，由上层解析和发送，这个行为透传给上层处理


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| parameters | [ADTrackActionModel.ParametersEntry](#riaid.ADTrackActionModel.ParametersEntry) | repeated | 例如：[actionType=2, templateType=1] |






<a name="riaid.ADTrackActionModel.ParametersEntry"></a>

### ADTrackActionModel.ParametersEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [string](#string) |  |  |






<a name="riaid.ADTransitionActionModel"></a>

### ADTransitionActionModel
所有Transition的行为，通常用于场景的转场或场景内动画


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [int32](#int32) |  | 作为唯一标识 |
| transitions | [ADTransitionModel](#riaid.ADTransitionModel) | repeated | Transition数组 |






<a name="riaid.ADTransitionModel"></a>

### ADTransitionModel
所有TransitionModel的封装类
注意，这里面的成员只能有一个，因为客户端使用的MessageNano，因为解析原因，暂不使用oneof


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| visibility | [ADVisibilityTransitionModel](#riaid.ADVisibilityTransitionModel) |  | 场景可见性转场描述 |
| template | [ADTemplateTransitionModel](#riaid.ADTemplateTransitionModel) |  | 场景模板转场描述 |
| translation | [ADTranslationTransitionModel](#riaid.ADTranslationTransitionModel) |  | 场景位置更改转场描述 |
| in_scene_animation | [ADInSceneAnimationTransitionModel](#riaid.ADInSceneAnimationTransitionModel) |  | 场景内的转场动画 |
| scene_share | [ADSceneShareTransitionModel](#riaid.ADSceneShareTransitionModel) |  | 场景与场景的共享元素转场过渡动画 |
| lottie | [ADLottieTransitionModel](#riaid.ADLottieTransitionModel) |  | LottieTransitionModel |
| render_content | [ADRenderContentTransitionModel](#riaid.ADRenderContentTransitionModel) |  | 场景内的特定Transition，用于更新render的内容 |






<a name="riaid.ADTranslationTransitionModel"></a>

### ADTranslationTransitionModel
场景位置更改转场描述


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| scene_key | [int32](#int32) |  |  |
| duration | [int64](#int64) |  |  |
| scene_relations | [ADSceneRelationModel](#riaid.ADSceneRelationModel) | repeated |  |






<a name="riaid.ADTriggerActionModel"></a>

### ADTriggerActionModel
触发一个Trigger


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| trigger_keys | [int32](#int32) | repeated |  |






<a name="riaid.ADTriggerModel"></a>

### ADTriggerModel
所有Trigger的封装类
注意，这里面的成员只能有一个，因为客户端使用的MessageNano，因为解析原因，暂不使用oneof


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| timeout | [ADTimeoutTriggerModel](#riaid.ADTimeoutTriggerModel) |  | 定时触发器，例如：3秒后触发操作 |
| heartbeat | [ADHeartBeatTriggerModel](#riaid.ADHeartBeatTriggerModel) |  | 心跳触发器，例如：每隔3秒，触发操作 |
| general | [ADGeneralTriggerModel](#riaid.ADGeneralTriggerModel) |  | 普通触发器 |
| condition | [ADConditionTriggerModel](#riaid.ADConditionTriggerModel) |  | 代表一个不确定的操作，需要根据当时的环境变量，来确定具体的操作 |
| videoDuration | [ADVideoDurationTimeoutTriggerModel](#riaid.ADVideoDurationTimeoutTriggerModel) |  | video计时器的触发器，用来匹配一个video的播放时间，来触发行为 |






<a name="riaid.ADUrlActionModel"></a>

### ADUrlActionModel
url的Action，如直接跳转落地的，这个行为透传给上层处理


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| url | [string](#string) |  | 要跳转的url |
| bundle | [ADUrlActionModel.BundleEntry](#riaid.ADUrlActionModel.BundleEntry) | repeated | 可能要透传的打包数据 |






<a name="riaid.ADUrlActionModel.BundleEntry"></a>

### ADUrlActionModel.BundleEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [string](#string) |  |  |






<a name="riaid.ADVariableChangeActionModel"></a>

### ADVariableChangeActionModel
变量变化的action


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| variable | [BasicVariable](#riaid.BasicVariable) |  | 变量模型 |






<a name="riaid.ADVideoActionModel"></a>

### ADVideoActionModel
视频播放控制的Action，这个行为透传给上层处理


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| type | [ADVideoActionModel.VideoControlType](#riaid.ADVideoActionModel.VideoControlType) |  |  |
| view_key | [int32](#int32) |  | scene_key render_key 都不等于0，才是内部的 |






<a name="riaid.ADVideoDurationTimeoutTriggerModel"></a>

### ADVideoDurationTimeoutTriggerModel
Video计时器，Time Source是播放器，而不是系统


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [int32](#int32) |  | 触发器的key |
| view_key | [int32](#int32) |  | 播放器的key，也可以是外部播放器的key |
| interval | [int64](#int64) |  | 触发时机，单位毫秒，例：time=1000，则为1s后触发 |
| actions | [ADActionModel](#riaid.ADActionModel) | repeated | Action集合 |
| debug_info | [string](#string) |  | 用来说明该触发器是做什么用的，简单描述。 |






<a name="riaid.ADVisibilityTransitionModel"></a>

### ADVisibilityTransitionModel
场景可见性转场描述


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| scene_key | [int32](#int32) |  | Transition对应的场景 |
| duration | [int64](#int64) |  | ms，动画执行的时间 |
| start_alpha | [float](#float) |  | [0-1] |
| end_alpha | [float](#float) |  |  |
| hidden | [bool](#bool) |  | 目标状态要求是可见还是不可见 |






<a name="riaid.Attributes"></a>

### Attributes



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| common | [CommonAttributes](#riaid.CommonAttributes) |  |  |
| text | [TextAttributes](#riaid.TextAttributes) |  |  |
| image | [ImageAttributes](#riaid.ImageAttributes) |  |  |
| lottie | [LottieAttributes](#riaid.LottieAttributes) |  |  |
| scroll | [ScrollAttributes](#riaid.ScrollAttributes) |  |  |
| button | [ButtonAttributes](#riaid.ButtonAttributes) |  |  |
| video | [VideoAttributes](#riaid.VideoAttributes) |  |  |






<a name="riaid.BasicVariable"></a>

### BasicVariable
变量定义，此变量为全局变量


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [int32](#int32) |  | 变量的地址，也是唯一标识，要求大于等于零 |
| name | [string](#string) |  | 变量的名字，可以为空 |
| value | [BasicVariableValue.Value](#riaid.BasicVariableValue.Value) |  | 变量的具体值 |






<a name="riaid.BasicVariableValue"></a>

### BasicVariableValue







<a name="riaid.BasicVariableValue.Value"></a>

### BasicVariableValue.Value



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| type | [BasicVariableValue.Type](#riaid.BasicVariableValue.Type) |  |  |
| b | [bool](#bool) |  | 布尔类型，默认是false |
| i | [int64](#int64) |  | integer 类型统一定义为 int64 类型，默认是0 |
| d | [double](#double) |  | 浮点类型 统一定义为 double 类型,默认是0.0 |
| s | [string](#string) |  | 字符串类型 默认是nil |






<a name="riaid.BoolValue"></a>

### BoolValue
Bool 的内部定义。因为目前我们使用的 Protobuff 不支持 optional 定义。而在某些场景下需要定义空值的数据。
因而我们使用这个方式，来达到 optional 的目的。


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| value | [bool](#bool) |  |  |






<a name="riaid.ButtonAttributes"></a>

### ButtonAttributes



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| content | [Node](#riaid.Node) |  |  |
| highlight_state_list | [ButtonAttributes.HighlightState](#riaid.ButtonAttributes.HighlightState) | repeated |  |






<a name="riaid.ButtonAttributes.HighlightState"></a>

### ButtonAttributes.HighlightState



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [int32](#int32) |  |  |
| attributes | [Attributes](#riaid.Attributes) |  |  |






<a name="riaid.CommonAttributes"></a>

### CommonAttributes
这个是基础通用属性


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| shape_type | [CommonAttributes.ShapeType](#riaid.CommonAttributes.ShapeType) |  |  |
| corner_radius | [CornerRadius](#riaid.CornerRadius) |  | 背景圆角 |
| background_color | [string](#string) |  | 背景色 ARGB 8位16进制 |
| gradient | [Gradient](#riaid.Gradient) |  | 渐变 |
| stroke | [Stroke](#riaid.Stroke) |  | 边框线 |
| shadow | [Shadow](#riaid.Shadow) |  | 阴影 |
| alpha | [FloatValue](#riaid.FloatValue) |  | 透明度,0~1数值越小越透明 |
| hidden | [BoolValue](#riaid.BoolValue) |  | 是否隐藏不可见 |






<a name="riaid.CornerRadius"></a>

### CornerRadius
圆角属性控制。通过这个对象，可以控制控件的圆角属性。


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| top_start | [float](#float) |  |  |
| bottom_start | [float](#float) |  |  |
| top_end | [float](#float) |  |  |
| bottom_end | [float](#float) |  |  |






<a name="riaid.FloatValue"></a>

### FloatValue
Float 的内部定义。因为目前我们使用的 Protobuff 不支持 optional 定义。而在某些场景下需要定义空值的数据。
因而我们使用这个方式，来达到 optional 的目的。


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| value | [float](#float) |  |  |






<a name="riaid.Gradient"></a>

### Gradient
渐变属性控制。通过这个对象，可以控制控件的渐变属性。


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| type | [Gradient.GradientType](#riaid.Gradient.GradientType) |  |  |
| angle | [Gradient.GradientAngle](#riaid.Gradient.GradientAngle) |  | 这个定义枚举过于费力，只能从上诉角度选择 |
| colors | [string](#string) | repeated |  |






<a name="riaid.Handler"></a>

### Handler



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| click | [Responder](#riaid.Responder) |  |  |
| double_click | [Responder](#riaid.Responder) |  |  |
| long_press | [Responder](#riaid.Responder) |  |  |






<a name="riaid.ImageAttributes"></a>

### ImageAttributes



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| url | [string](#string) |  |  |
| highlight_url | [string](#string) |  |  |
| scale_type | [ImageAttributes.ScaleType](#riaid.ImageAttributes.ScaleType) |  | 有以下集中形式 |






<a name="riaid.Int32Value"></a>

### Int32Value
Int32 的内部定义。因为目前我们使用的 Protobuff 不支持 optional 定义。而在某些场景下需要定义空值的数据。
因而我们使用这个方式，来达到 optional 的目的。


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| value | [int32](#int32) |  |  |






<a name="riaid.Layout"></a>

### Layout
布局属性，通过 Layout 可以控制一个控件在界面上的布局属性。


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| priority | [int32](#int32) |  | 优先级 |
| weight | [int32](#int32) |  | 权重，用来均分剩余空间的 |
| margin | [Layout.Edge](#riaid.Layout.Edge) |  | 组件和组件的距离 |
| padding | [Layout.Edge](#riaid.Layout.Edge) |  | 组件的内部边距 |
| width | [float](#float) |  | 实际服务端下发尺寸 |
| height | [float](#float) |  | 实际服务端下发宽度 |






<a name="riaid.Layout.Edge"></a>

### Layout.Edge



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| start | [float](#float) |  | 横向开始 |
| end | [float](#float) |  | 横向结束 |
| top | [float](#float) |  | 纵向顶部 |
| bottom | [float](#float) |  | 纵向底部 |






<a name="riaid.LottieAttributes"></a>

### LottieAttributes



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| url | [string](#string) |  | lottie的链接地址 |
| speed | [FloatValue](#riaid.FloatValue) |  | lottie播放速度 |
| progress | [FloatValue](#riaid.FloatValue) |  | 默认开始进度 0~1 |
| repeat | [BoolValue](#riaid.BoolValue) |  | 是否重复播放，如果否就只播放一次 |
| repeat_mode | [LottieAttributes.RepeatMode](#riaid.LottieAttributes.RepeatMode) |  | 重复播放的模式 |
| auto_play | [BoolValue](#riaid.BoolValue) |  | 是否要重新开始播放 |
| replace_text_list | [LottieAttributes.ReplaceText](#riaid.LottieAttributes.ReplaceText) | repeated | 文本替换 |






<a name="riaid.LottieAttributes.ReplaceText"></a>

### LottieAttributes.ReplaceText



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| place_holder | [string](#string) |  | 需要被替换的lottie里面的文本 |
| real_text | [string](#string) |  | 需要被展示的目标文本 |






<a name="riaid.Node"></a>

### Node



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| class_type | [Node.ClassType](#riaid.Node.ClassType) |  | 当前组件的类型 |
| key | [int32](#int32) |  | 当前组件的唯一标识 当前组件的唯一标识 |
| layout | [Layout](#riaid.Layout) |  | 当前组件的布局属性，尺寸，距离等 |
| handler | [Handler](#riaid.Handler) |  | 当前组件的响应的行为 |
| attributes | [Attributes](#riaid.Attributes) |  | 当前组件的样式属性 |
| children | [Node](#riaid.Node) | repeated | 子组件，只有盒子布局这个属性才会有意义 |
| debug_info | [string](#string) |  | 用来说明该Node是做什么用的，简单描述 |
| video_handler | [VideoHandler](#riaid.VideoHandler) |  | 视频的监听 |






<a name="riaid.Responder"></a>

### Responder



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| trigger_keys | [int32](#int32) | repeated | triggerKey数组 |






<a name="riaid.RiaidModel"></a>

### RiaidModel
广告dsl配置的数据模型，输入到ADDirector中


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| life_cycle | [ADBrowserLifeCycleModel](#riaid.ADBrowserLifeCycleModel) |  | ADBrowser生命周期 |
| scenes | [ADSceneModel](#riaid.ADSceneModel) | repeated | 所有的场景集合 |
| default_scene_relations | [ADSceneRelationModel](#riaid.ADSceneRelationModel) | repeated | scene的位置关系，用于定义scene在整个广告画布中的位置，用正则表达式解析。 |
| triggers | [ADTriggerModel](#riaid.ADTriggerModel) | repeated | 触发器集合，所有触发器提前在此下发，之后再使用，直接用TriggerKey调用。 |
| default_conditions | [ADConditionModel](#riaid.ADConditionModel) | repeated | 起始默认的条件。作用类似环境变量，用作表述当前的状态。作为不确定操作的判断依据。 |
| default_variables | [BasicVariable](#riaid.BasicVariable) | repeated | 起始默认的变量，可被操作的所有的全局变量 |
| functions | [ADFunctionModel](#riaid.ADFunctionModel) | repeated | 内置函数集合，所有函数提前在此下发，之后使用，可通过#functionKey调用 |






<a name="riaid.ScrollAttributes"></a>

### ScrollAttributes



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| show_scrollbar | [BoolValue](#riaid.BoolValue) |  |  |






<a name="riaid.Shadow"></a>

### Shadow
阴影


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| offset_x | [float](#float) |  | 水平偏移量 |
| offset_y | [float](#float) |  | 垂直偏移量 |
| color | [string](#string) |  | 颜色，很好理解bro |
| radius | [float](#float) |  | 半径 |






<a name="riaid.Stroke"></a>

### Stroke
边框线


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| width | [float](#float) |  | 边框宽度 |
| color | [string](#string) |  | 边框颜色 |
| dash_width | [float](#float) |  | 虚线的宽度，0代表实线 |
| dash_gap | [float](#float) |  | 虚线的间隔 |






<a name="riaid.SystemKeyEnum"></a>

### SystemKeyEnum







<a name="riaid.TextAttributes"></a>

### TextAttributes



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| text | [string](#string) |  |  |
| font_size | [FloatValue](#riaid.FloatValue) |  |  |
| font_name | [string](#string) |  |  |
| font_color | [string](#string) |  |  |
| max_lines | [Int32Value](#riaid.Int32Value) |  |  |
| ellipsize | [TextAttributes.Ellipsize](#riaid.TextAttributes.Ellipsize) |  |  |
| align | [TextAttributes.Align](#riaid.TextAttributes.Align) |  |  |
| bold | [BoolValue](#riaid.BoolValue) |  | 是否加粗 |
| tilt | [BoolValue](#riaid.BoolValue) |  | 是否斜体 |
| line_mode | [TextAttributes.LineMode](#riaid.TextAttributes.LineMode) |  |  |
| line_space | [FloatValue](#riaid.FloatValue) |  | 行间距 |
| highlight_color | [string](#string) |  | 按压态的高亮色 |
| rich_list | [TextAttributes.RichText](#riaid.TextAttributes.RichText) | repeated | 富文本集合 |






<a name="riaid.TextAttributes.Align"></a>

### TextAttributes.Align
对齐方式


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| horizontal | [TextAttributes.Align.Horizontal](#riaid.TextAttributes.Align.Horizontal) |  | start end center_horizontal |
| vertical | [TextAttributes.Align.Vertical](#riaid.TextAttributes.Align.Vertical) |  | top bottom center_vertical |






<a name="riaid.TextAttributes.RichText"></a>

### TextAttributes.RichText
富文本


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| place_holder | [string](#string) |  | 匹配文本 |
| content | [Node](#riaid.Node) |  | 内容 |
| handler | [Handler](#riaid.Handler) |  | 响应行为 |






<a name="riaid.VideoAttributes"></a>

### VideoAttributes
新增Video属性对象


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| auto_mute | [BoolValue](#riaid.BoolValue) |  | 是否静音 |
| auto_loop | [BoolValue](#riaid.BoolValue) |  | 是否循环播放 |
| auto_seek_time | [int64](#int64) |  | 视频进度，理解为seek |
| auto_play | [BoolValue](#riaid.BoolValue) |  | 是否自动播放 |
| url | [string](#string) |  | 视频链接 |
| cover_url | [string](#string) |  | 首帧图片 |






<a name="riaid.VideoHandler"></a>

### VideoHandler
这个是视频控件独有的，不通用，不放在点击的Handler里面


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| impression | [Responder](#riaid.Responder) |  | 首帧 |
| finish | [Responder](#riaid.Responder) |  | 播放完成 |
| pause | [Responder](#riaid.Responder) |  | 播放暂停 |
| start | [Responder](#riaid.Responder) |  | 播放 |
| resume | [Responder](#riaid.Responder) |  | 将暂停的video播放 |








<a name="riaid.ADAnimationModel.ViewPropertyType"></a>

### ADAnimationModel.ViewPropertyType
视图的一些属性

| Name | Number | Description |
| ---- | ------ | ----------- |
| VIEW_PROPERTY_NONE | 0 |  |
| ALPHA | 1 | 参考{@link android.view.View#ALPHA} |
| SCALE | 2 | 参考{@link android.view.View#SCALE_X}+{@link android.view.View#SCALE_Y} |
| ROTATION | 3 | 参考{@link android.view.View#ROTATION} |
| WIDTH | 4 | 持续更改View宽度的{@link android.animation.ValueAnimator} 当等于-1则认为是view经过计算后的值 |
| HEIGHT | 5 | 持续更改View高度的{@link android.animation.ValueAnimator} 当等于-1则认为是view经过计算后的值 |
| HIDDEN | 6 | values长度是1，只有一个值 可见，可响应点击事件,value = 0 不可见，会占用空间，但不能响应点击事件，value = 1 |



<a name="riaid.ADSceneRelationModel.SceneEdge"></a>

### ADSceneRelationModel.SceneEdge


| Name | Number | Description |
| ---- | ------ | ----------- |
| SCENE_EDGE_NONE | 0 |  |
| START | 1 | 左边，RTL为右边 |
| TOP | 2 | 上边 |
| END | 3 | 右边，RTL为左边 |
| BOTTOM | 4 | 下边 |



<a name="riaid.ADTemplateTransitionModel.TemplateType"></a>

### ADTemplateTransitionModel.TemplateType


| Name | Number | Description |
| ---- | ------ | ----------- |
| TEMPLATE_TYPE_NONE | 0 |  |
| ENTER_FROM_START | 1 | 从左边进入 |
| EXIT_FROM_START | 2 | 从左边移出 |



<a name="riaid.ADVideoActionModel.VideoControlType"></a>

### ADVideoActionModel.VideoControlType


| Name | Number | Description |
| ---- | ------ | ----------- |
| VIDEO_NONE | 0 |  |
| VIDEO_REPLAY | 1 | 重新播放视频 |
| VIDEO_POSITION_RESET | 2 | 视频得到位置回到首帧，但不会重新播放 |
| VIDEO_PAUSE | 3 | 新增暂停视频能力 |
| VIDEO_PLAY | 4 | 新增继续播放控制能力 |
| VIDEO_SOUND_TURN_ON | 5 | 静音 |
| VIDEO_SOUND_TURN_OFF | 6 | 解除静音 |



<a name="riaid.Attributes.AttributeType"></a>

### Attributes.AttributeType


| Name | Number | Description |
| ---- | ------ | ----------- |
| ATTRIBUTE_UNKNOWN | 0 | 未知属性 |
| ATTRIBUTE_VIDEO_POSITION | 1 | 视频的当前播放位置，单位：ms |
| ATTRIBUTE_VIDEO_TOTAL_DURATION | 2 | 视频的总播放时长，累加，单位：ms

.... 其他属性类型待扩展 |



<a name="riaid.BasicVariableValue.Type"></a>

### BasicVariableValue.Type
变量支持的类型，包括布尔，长整形，double和字符串

| Name | Number | Description |
| ---- | ------ | ----------- |
| NONE | 0 |  |
| BOOL | 1 |  |
| INTEGER | 2 |  |
| DOUBLE | 3 |  |
| STRING | 4 |  |



<a name="riaid.CommonAttributes.ShapeType"></a>

### CommonAttributes.ShapeType


| Name | Number | Description |
| ---- | ------ | ----------- |
| SHAPE_TYPE_UNKNOWN | 0 |  |
| SHAPE_TYPE_RECTANGLE | 1 |  |



<a name="riaid.CompareOperator"></a>

### CompareOperator
比较运算符

| Name | Number | Description |
| ---- | ------ | ----------- |
| COMPARE_OPERATOR_UNKNOWN | 0 | 不识别 |
| COMPARE_OPERATOR_EQUAL | 1 | 相等 |
| COMPARE_OPERATOR_NOT_EQUAL | 2 | 不相等 |
| COMPARE_OPERATOR_LESS_THAN | 3 | 小于 |
| COMPARE_OPERATOR_GREATER_THAN | 4 | 大于 |
| COMPARE_OPERATOR_LESS_THAN_OR_EQUAL | 5 | 小于等于 |
| COMPARE_OPERATOR_GREATER_THAN_OR_EQUAL | 6 | 大于等于 |



<a name="riaid.Gradient.GradientAngle"></a>

### Gradient.GradientAngle


| Name | Number | Description |
| ---- | ------ | ----------- |
| ANGLE_UNKNOWN | 0 |  |
| ANGLE_0 | 1 | 0 左--> 右 |
| ANGLE_45 | 2 | 45 左下 --> 右上 |
| ANGLE_90 | 3 | 90 下 --> 上 |
| ANGLE_135 | 4 | 135 右下 --> 左上 |
| ANGLE_180 | 5 | 180 右 --> 左 |
| ANGLE_225 | 6 | 225 右上 --> 左下 |
| ANGLE_270 | 7 | 270 上 --> 下 |
| ANGLE_315 | 8 | 315 左上 --> 右下 |



<a name="riaid.Gradient.GradientType"></a>

### Gradient.GradientType
渐变类型。目前我们仅支持三种渐变类型。

| Name | Number | Description |
| ---- | ------ | ----------- |
| GRADIENT_TYPE_UNKNOWN | 0 |  |
| GRADIENT_TYPE_LINEAR | 1 |  |



<a name="riaid.ImageAttributes.ScaleType"></a>

### ImageAttributes.ScaleType


| Name | Number | Description |
| ---- | ------ | ----------- |
| SCALE_TYPE_UNKNOWN | 0 |  |
| SCALE_TYPE_FIT_XY | 1 |  |
| SCALE_TYPE_FIT_END | 2 |  |
| SCALE_TYPE_FIT_START | 3 |  |
| SCALE_TYPE_FIT_CENTER | 4 |  |
| SCALE_TYPE_CENTER | 5 |  |
| SCALE_TYPE_CENTER_CROP | 6 |  |



<a name="riaid.LogicOperator"></a>

### LogicOperator
逻辑运算符-与、或、非

| Name | Number | Description |
| ---- | ------ | ----------- |
| LOGIC_OPERATOR_UNKNOWN | 0 | 不识别 |
| LOGIC_OPERATOR_OR | 1 | 或 |
| LOGIC_OPERATOR_AND | 2 | 与 |
| LOGIC_OPERATOR_NOT | 3 | 非 |



<a name="riaid.LottieAttributes.RepeatMode"></a>

### LottieAttributes.RepeatMode


| Name | Number | Description |
| ---- | ------ | ----------- |
| REPEAT_MODE_UNKNOWN | 0 |  |
| REPEAT_MODE_RESTART | 1 | 重新开始播放 |
| REPEAT_MODE_REVERSE | 2 | 播放结束，倒退播放 |



<a name="riaid.Node.ClassType"></a>

### Node.ClassType
可支持点击等事件的类型：1，2，4，6

| Name | Number | Description |
| ---- | ------ | ----------- |
| CLASS_TYPE_UNKNOWN | 0 |  |
| CLASS_TYPE_ITEM_IMAGE | 1 | 子组件 |
| CLASS_TYPE_ITEM_LOTTIE | 2 |  |
| CLASS_TYPE_ITEM_SPACE | 3 |  |
| CLASS_TYPE_ITEM_TEXT | 4 |  |
| CLASS_TYPE_LAYOUT_ABSOLUTE | 5 | 盒子组件 |
| CLASS_TYPE_LAYOUT_BUTTON | 6 |  |
| CLASS_TYPE_LAYOUT_HORIZONTAL | 7 |  |
| CLASS_TYPE_LAYOUT_H_SCROLL | 8 |  |
| CLASS_TYPE_LAYOUT_SQUARE | 9 |  |
| CLASS_TYPE_LAYOUT_VERTICAL | 10 |  |
| CLASS_TYPE_LAYOUT_V_SCROLL | 11 |  |
| CLASS_TYPE_ITEM_VIDEO | 12 |  |



<a name="riaid.SystemKeyEnum.SystemKeys"></a>

### SystemKeyEnum.SystemKeys


| Name | Number | Description |
| ---- | ------ | ----------- |
| INVALID_KEY | 0 | 无效的key，适用于Riaid数据模型中定义的所有key，例:viewKey、sceneKe、triggerKey等 |
| TRIGGER_KEY_AD_VIDEO_END | -6662 | 视频播放结束的内置触发器的key |
| SCENE_KEY_CANVAS | -6661 | 如果sceneKey是SCENE_KEY_CANVAS，认为是画布 |



<a name="riaid.TextAttributes.Align.Horizontal"></a>

### TextAttributes.Align.Horizontal


| Name | Number | Description |
| ---- | ------ | ----------- |
| HORIZONTAL_UNKNOWN | 0 |  |
| HORIZONTAL_START | 1 |  |
| HORIZONTAL_CENTER | 2 |  |
| HORIZONTAL_END | 3 |  |



<a name="riaid.TextAttributes.Align.Vertical"></a>

### TextAttributes.Align.Vertical


| Name | Number | Description |
| ---- | ------ | ----------- |
| VERTICAL_UNKNOWN | 0 |  |
| VERTICAL_TOP | 1 |  |
| VERTICAL_CENTER | 2 |  |
| VERTICAL_BOTTOM | 3 |  |



<a name="riaid.TextAttributes.Ellipsize"></a>

### TextAttributes.Ellipsize


| Name | Number | Description |
| ---- | ------ | ----------- |
| ELLIPSIZE_UNKNOWN | 0 |  |
| ELLIPSIZE_START | 1 |  |
| ELLIPSIZE_MIDDLE | 2 |  |
| ELLIPSIZE_END | 3 |  |



<a name="riaid.TextAttributes.LineMode"></a>

### TextAttributes.LineMode
下划线控制

| Name | Number | Description |
| ---- | ------ | ----------- |
| LINE_MODE_UNKNOWN | 0 |  |
| LINE_MODE_NORMAL | 1 |  |
| LINE_MODE_UNDERLINE | 2 |  |
| LINE_MODE_STRIKE_THRU | 3 |  |










## Scalar Value Types

| .proto Type | Notes | C++ | Java | Python | Go | C# | PHP | Ruby |
| ----------- | ----- | --- | ---- | ------ | -- | -- | --- | ---- |
| <a name="double" /> double |  | double | double | float | float64 | double | float | Float |
| <a name="float" /> float |  | float | float | float | float32 | float | float | Float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum or Fixnum (as required) |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="bool" /> bool |  | bool | boolean | boolean | bool | bool | boolean | TrueClass/FalseClass |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode | string | string | string | String (UTF-8) |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str | []byte | ByteString | string | String (ASCII-8BIT) |
