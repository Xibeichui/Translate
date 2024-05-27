
### DownloadedLanguageDialog 组件说明：

DownloadedLanguageDialog 组件的主要用途是显示已下载语言列表，以供用户查看和管理。

#### 属性：

- `downloadedList: List<String>`：已下载语言的列表。包含用户已经下载的语言模型，用于显示在对话框中。
- `expanded: MutableState<Boolean>`：控制对话框是否展开的状态。通过修改该状态，可以显示或隐藏对话框。
- `onLanguageChanged: (Language) -> Unit`：当语言被更改时调用的回调函数。用户选择不同语言时触发该回调，以便应用进行相应的处理（例如切换翻译语言）。
- `onDownloadClicked: (String) -> Unit`：当下载按钮被点击时调用的回调函数。用户点击下载按钮后触发该回调，以便应用开始下载新的语言模型。
- `isTargetLanguage: Boolean`：是否为目标语言，默认为 false。该属性用于区分对话框是用于设置目标语言还是源语言。

#### 方法：

- `displayDialog()`: Unit：显示已下载语言对话框。

![image](https://github.com/Xibeichui/Translate/assets/134084828/d388c50e-5b48-4273-b5b5-45140f44f9d2)


---

### LanguageInfo 组件说明：

LanguageInfo 组件主要用于显示单个语言的信息，提供了语言名称、是否已下载以及相关操作的回调函数，以便用户与语言进行交互。

#### 属性：

- `language: String`：语言名称。
- `context: Context`：Android 上下文对象。
- `isDownload: Boolean`：是否已下载。
- `onDownloadClicked: (String) -> Unit`：当下载按钮被点击时调用的回调函数。
- `onCardClicked: () -> Unit`：当语言卡片被点击时调用的回调函数。

#### 方法：

- `getLanguage(): String`：获取语言名称。
- `getContext(): Context`：获取上下文对象。
- `isDownloaded(): Boolean`：检查语言是否已下载。
- `setOnDownloadClickedListener(onClick: (String) -> Unit): Unit`：设置下载按钮点击事件监听器。
- `setOnCardClickedListener(onClick: () -> Unit): Unit`：设置语言卡片点击事件监听器。

![image](https://github.com/Xibeichui/Translate/assets/134084828/ebf56c93-e46f-4b97-8e10-afb123d432d6)

---

### DropDownMenu 组件说明：

DropDownMenu 是一个用于选择字符类型的下拉菜单组件。

#### 属性：

- `modifier: Modifier`：可选的修饰符，用于自定义组件的外观和行为。
- `setCharacter: (Character) -> Unit`：设置字符类型的回调函数。当用户选择了一个字符类型时，该回调函数会被调用，传递选择的字符类型作为参数。
- `characterType: Character`：当前选择的字符类型。

#### 方法：

- `displayMenu()`: Unit：显示下拉菜单。当用户点击下拉菜单时，会调用该方法以显示可选择的字符类型列表。

![image](https://github.com/Xibeichui/Translate/assets/134084828/534e9b58-27bd-469e-ae8f-c5ecfdb99c1a)


---

### LanguageCard 组件说明：

LanguageCard 是一个用于显示语言名称和图标的组件。

#### 属性：

- `language: Language`：要显示的语言对象。
- `modifier: Modifier`：可选的修饰符，用于自定义组件的外观和行为。
- `textColor: Color`：文字颜色，默认为黑色。

#### 方法：

- `displayCard()`: Unit：显示语言卡片。当调用此方法时，将显示语言的名称和图标。

![image](https://github.com/Xibeichui/Translate/assets/134084828/d0c59642-cb38-4bde-8293-3fbbce8ac708)

