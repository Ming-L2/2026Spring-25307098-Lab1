工程目录注释
scankit-samplecode-clientdemo-arkts-master/
├── .hvigor/                      # 构建缓存目录
│   └── 存放Hvigor构建系统的缓存文件，包括编译中间产物和依赖缓存
├── .idea/                        # IDE配置文件目录
│   └── IntelliJ IDEA/DevEco Studio项目配置文件，包括运行配置、代码样式等
├── AppScope/                     # 应用级作用域配置
│   ├── app.json5                 # 应用配置文件 - 定义应用基本信息
│   │   ├── bundleName: 应用包名标识符
│   │   ├── vendor: 开发者信息
│   │   ├── versionCode/versionName: 版本管理
│   │   └── icon/label: 应用图标和显示名称
│   └── resources/                # 全局资源文件
│       ├── base/element/string.json  # 应用级字符串资源
│       ├── base/media/app_icon.png   # 应用图标
│       └── base/profile/configuration.json  # 应用配置
├── entry/                        # 主模块（入口模块）
│   ├── src/main/
│   │   ├── ets/                  # ArkTS源代码（核心业务逻辑）
│   │   │   ├── common/           # 公共组件和工具
│   │   │   │   ├── CommonComponents.ets    # 自定义按钮组件
│   │   │   │   ├── CommonTipsDialog.ets    # 通用提示对话框
│   │   │   │   ├── PermissionsUtil.ets     # 权限管理工具
│   │   │   │   ├── StatusBar.ets           # 状态栏组件
│   │   │   │   └── Utils.ets               # 通用工具函数
│   │   │   ├── entryability/     # 应用入口能力
│   │   │   │   └── EntryAbility.ets        # 应用生命周期管理
│   │   │   ├── pages/            # 页面组件（按功能模块组织）
│   │   │   │   ├── Index.ets               # 应用主入口页面
│   │   │   │   ├── access/                 # 扫码直达服务模块
│   │   │   │   │   ├── ScanAccess.ets      # 扫码直达入口页面
│   │   │   │   │   └── ScanDetail.ets      # 扫码直达详情页面
│   │   │   │   ├── customScan/             # 自定义扫码模块（状态管理V1）
│   │   │   │   │   ├── constants/          # 常量定义
│   │   │   │   │   │   └── BreakpointConstants.ets  # 断点常量
│   │   │   │   │   ├── model/              # 业务模型层
│   │   │   │   │   │   ├── BreakpointType.ets       # 断点类型枚举
│   │   │   │   │   │   ├── DeviceService.ets        # 设备服务
│   │   │   │   │   │   ├── OpenPhoto.ets            # 打开相册功能
│   │   │   │   │   │   ├── ScanLayout.ets           # 扫码布局管理
│   │   │   │   │   │   ├── ScanService.ets          # 扫码核心服务
│   │   │   │   │   │   ├── UIContextSelf.ets        # UI上下文管理
│   │   │   │   │   │   ├── WindowService.ets        # 窗口服务
│   │   │   │   │   │   └── XComponentService.ets    # XComponent服务
│   │   │   │   │   ├── pages/              # 页面组件
│   │   │   │   │   │   └── ScanPage.ets             # 自定义扫码主页面
│   │   │   │   │   ├── view/               # 视图组件
│   │   │   │   │   │   ├── CommonCodeLayout.ets     # 通用码布局
│   │   │   │   │   │   ├── IconPress.ets            # 图标按压效果
│   │   │   │   │   │   ├── MaskLayer.ets            # 遮罩层组件
│   │   │   │   │   │   ├── PickerDialog.ets         # 选择器对话框
│   │   │   │   │   │   ├── ScanBottom.ets           # 扫码底部栏
│   │   │   │   │   │   ├── ScanLine.ets             # 扫码线动画
│   │   │   │   │   │   ├── ScanLoading.ets          # 加载动画
│   │   │   │   │   │   ├── ScanTitle.ets            # 扫码标题栏
│   │   │   │   │   │   └── ScanXComponent.ets       # XComponent相机预览
│   │   │   │   │   └── CustomPage.ets               # 自定义扫码入口页面
│   │   │   │   ├── customScanV2/           # 自定义扫码模块（状态管理V2）
│   │   │   │   │   ├── model/              # V2业务模型层
│   │   │   │   │   │   ├── ConfigStorage.ets        # 配置存储
│   │   │   │   │   │   ├── OpenPhoto.ets            # 打开相册功能
│   │   │   │   │   │   ├── ScanLayout.ets           # 扫码布局管理
│   │   │   │   │   │   ├── ScanService.ets          # V2扫码服务
│   │   │   │   │   │   ├── WindowService.ets        # 窗口服务
│   │   │   │   │   │   └── XComponentService.ets    # XComponent服务
│   │   │   │   │   ├── pages/              # V2页面组件
│   │   │   │   │   │   └── ScanPage.ets             # V2扫码页面
│   │   │   │   │   └── view/               # V2视图组件（与V1类似）
│   │   │   │   ├── defaultScan/            # 默认扫码模块
│   │   │   │   │   └── DefaultScan.ets              # 系统默认扫码界面
│   │   │   │   ├── detectBarcode/          # 图像识码模块
│   │   │   │   │   ├── CommonCodeLayout.ets         # 通用码布局
│   │   │   │   │   ├── DecodeBarcode.ets            # 图片识码功能
│   │   │   │   │   └── DecodeCameraYuv.ets          # 相机YUV数据识别
│   │   │   │   ├── generateBarcode/        # 码图生成模块
│   │   │   │   │   └── CreateBarcode.ets            # 码图生成功能
│   │   │   │   └── resultPage/             # 结果展示模块
│   │   │   │       └── ResultPage.ets               # 扫码结果展示页面
│   │   │   └── utils/                      # 工具类（当前为空）
│   │   ├── resources/            # 模块资源文件
│   │   │   ├── base/element/     # 基础元素资源
│   │   │   │   ├── color.json    # 颜色定义
│   │   │   │   ├── float.json    # 尺寸定义
│   │   │   │   └── string.json   # 字符串资源（248个字符串项）
│   │   │   ├── base/media/       # 媒体资源
│   │   │   │   └── icon.png      # 模块图标
│   │   │   ├── base/profile/     # 配置文件
│   │   │   │   └── main_pages.json  # 页面路由配置（12个页面）
│   │   │   ├── rawfile/          # 原始资源文件
│   │   │   │   ├── access.jpg          # 扫码直达入口图片
│   │   │   │   ├── accessEs.jpg        # 西班牙语版入口图片
│   │   │   │   ├── di.ogg              # 提示音效
│   │   │   │   ├── scan_back.svg       # 返回图标
│   │   │   │   ├── scan_close.svg      # 关闭图标
│   │   │   │   ├── scan_line.png       # 扫码线图片
│   │   │   │   ├── scan_photo.svg      # 相册图标
│   │   │   │   ├── scan_selected.svg   # 选中图标
│   │   │   │   ├── scan_selected2.svg  # 选中图标2
│   │   │   │   └── scan_shadow.png     # 阴影图片
│   │   │   └── zh_CN/element/    # 中文资源
│   │   │       └── string.json   # 中文字符串资源
│   │   └── module.json5          # 模块配置文件
│   │       ├── name: 模块名称
│   │       ├── type: 模块类型（entry）
│   │       ├── mainElement: 主能力（EntryAbility）
│   │       ├── deviceTypes: 支持设备（phone, tablet）
│   │       ├── pages: 页面路由配置
│   │       ├── abilities: 能力配置
│   │       └── requestPermissions: 权限申请（相机、震动）
│   ├── build-profile.json5       # 模块构建配置
│   │   └── 模块级构建参数配置
│   └── oh-package.json5          # 模块依赖配置
│       └── 模块名称、版本和依赖声明
├── build-profile.json5           # 项目构建配置
│   ├── app: 应用级构建配置
│   │   ├── signingConfigs: 签名配置
│   │   ├── products: 产品配置
│   │   │   ├── compatibleSdkVersion: 兼容SDK版本
│   │   │   ├── targetSdkVersion: 目标SDK版本
│   │   │   └── runtimeOS: 运行系统
│   │   └── buildModeSet: 构建模式
│   └── modules: 模块列表
├── hvigorfile.ts                 # 构建脚本
│   └── Hvigor构建系统配置文件
├── oh-package.json5              # 项目依赖配置
│   └── 项目级依赖管理配置
└── OAT.xml                       # 开源许可证信息
    └── 开源组件许可证声明文件