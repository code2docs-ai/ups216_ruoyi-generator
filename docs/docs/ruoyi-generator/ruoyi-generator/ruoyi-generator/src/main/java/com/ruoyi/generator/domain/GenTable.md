# 基础信息

|      |      |
|------|------|
| 编码语言 | .java |
| 代码路径 | ruoyi-generator/ruoyi-generator/src/main/java/com/ruoyi/generator/domain/GenTable.java |
| 包名 | com.ruoyi.generator.domain |
| 依赖项 | ['java.util.List', 'javax.validation.Valid', 'javax.validation.constraints.NotBlank', 'org.apache.commons.lang3.ArrayUtils', 'com.ruoyi.common.constant.GenConstants', 'com.ruoyi.common.core.domain.BaseEntity', 'com.ruoyi.common.utils.StringUtils'] |
| 概述说明 | GenTable类生成表结构，含表名、描述、列信息、路径，支持子表、树表、CRUD操作。 |

# 说明

GenTable类用于生成表结构，主要包含表名、描述、列信息、生成路径等关键属性。该类支持处理子表、树表以及常见的CRUD操作，功能全面，适用于复杂表结构的生成与管理。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| GenTable | class | GenTable类用于生成表结构，包含表名、描述、列信息、生成路径等关键属性，支持子表、树表、CRUD操作。 |



## 类 GenTable

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | GenTable |
| 说明 | GenTable类用于生成表结构，包含表名、描述、列信息、生成路径等关键属性，支持子表、树表、CRUD操作。 |


### UML类图

```mermaid
classDiagram
    class BaseEntity {
        <<Interface>>
    }

    class GenTable {
        -Long serialVersionUID
        -Long tableId
        -String tableName
        -String tableComment
        -String subTableName
        -String subTableFkName
        -String className
        -String tplCategory
        -String packageName
        -String moduleName
        -String businessName
        -String functionName
        -String functionAuthor
        -int formColNum
        -String genType
        -String genPath
        -GenTableColumn pkColumn
        -GenTable subTable
        -List~GenTableColumn~ columns
        -String options
        -String treeCode
        -String treeParentCode
        -String treeName
        -String parentMenuId
        -String parentMenuName
        +Long getTableId()
        +void setTableId(Long tableId)
        +String getTableName()
        +void setTableName(String tableName)
        +String getTableComment()
        +void setTableComment(String tableComment)
        +String getSubTableName()
        +void setSubTableName(String subTableName)
        +String getSubTableFkName()
        +void setSubTableFkName(String subTableFkName)
        +String getClassName()
        +void setClassName(String className)
        +String getTplCategory()
        +void setTplCategory(String tplCategory)
        +String getPackageName()
        +void setPackageName(String packageName)
        +String getModuleName()
        +void setModuleName(String moduleName)
        +String getBusinessName()
        +void setBusinessName(String businessName)
        +String getFunctionName()
        +void setFunctionName(String functionName)
        +String getFunctionAuthor()
        +void setFunctionAuthor(String functionAuthor)
        +int getFormColNum()
        +void setFormColNum(int formColNum)
        +String getGenType()
        +void setGenType(String genType)
        +String getGenPath()
        +void setGenPath(String genPath)
        +GenTableColumn getPkColumn()
        +void setPkColumn(GenTableColumn pkColumn)
        +GenTable getSubTable()
        +void setSubTable(GenTable subTable)
        +List~GenTableColumn~ getColumns()
        +void setColumns(List~GenTableColumn~ columns)
        +String getOptions()
        +void setOptions(String options)
        +String getTreeCode()
        +void setTreeCode(String treeCode)
        +String getTreeParentCode()
        +void setTreeParentCode(String treeParentCode)
        +String getTreeName()
        +void setTreeName(String treeName)
        +String getParentMenuId()
        +void setParentMenuId(String parentMenuId)
        +String getParentMenuName()
        +void setParentMenuName(String parentMenuName)
        +boolean isSub()
        +static boolean isSub(String tplCategory)
        +boolean isTree()
        +static boolean isTree(String tplCategory)
        +boolean isCrud()
        +static boolean isCrud(String tplCategory)
        +boolean isSuperColumn(String javaField)
        +static boolean isSuperColumn(String tplCategory, String javaField)
    }

    class GenTableColumn {
        // 假设GenTableColumn类的定义
    }

    BaseEntity <|-- GenTable
    GenTable --> GenTableColumn : 包含
    GenTable --> GenTable : 包含
```

这段代码定义了一个`GenTable`类，继承自`BaseEntity`接口。`GenTable`类包含了多个属性，如`tableId`、`tableName`、`tableComment`等，并提供了相应的getter和setter方法。此外，`GenTable`类还包含了一些用于判断模板类型的方法，如`isSub`、`isTree`和`isCrud`。`GenTable`类与`GenTableColumn`类存在关联关系，表示表格的列信息。


### 内部方法调用关系图

```mermaid
graph TD
    A["类GenTable"]
    B["属性: Long tableId"]
    C["属性: String tableName"]
    D["属性: String tableComment"]
    E["属性: String subTableName"]
    F["属性: String subTableFkName"]
    G["属性: String className"]
    H["属性: String tplCategory"]
    I["属性: String packageName"]
    J["属性: String moduleName"]
    K["属性: String businessName"]
    L["属性: String functionName"]
    M["属性: String functionAuthor"]
    N["属性: int formColNum"]
    O["属性: String genType"]
    P["属性: String genPath"]
    Q["属性: GenTableColumn pkColumn"]
    R["属性: GenTable subTable"]
    S["属性: List<GenTableColumn> columns"]
    T["属性: String options"]
    U["属性: String treeCode"]
    V["属性: String treeParentCode"]
    W["属性: String treeName"]
    X["属性: String parentMenuId"]
    Y["属性: String parentMenuName"]
    Z["方法: Long getTableId()"]
    AA["方法: void setTableId(Long tableId)"]
    AB["方法: String getTableName()"]
    AC["方法: void setTableName(String tableName)"]
    AD["方法: String getTableComment()"]
    AE["方法: void setTableComment(String tableComment)"]
    AF["方法: String getSubTableName()"]
    AG["方法: void setSubTableName(String subTableName)"]
    AH["方法: String getSubTableFkName()"]
    AI["方法: void setSubTableFkName(String subTableFkName)"]
    AJ["方法: String getClassName()"]
    AK["方法: void setClassName(String className)"]
    AL["方法: String getTplCategory()"]
    AM["方法: void setTplCategory(String tplCategory)"]
    AN["方法: String getPackageName()"]
    AO["方法: void setPackageName(String packageName)"]
    AP["方法: String getModuleName()"]
    AQ["方法: void setModuleName(String moduleName)"]
    AR["方法: String getBusinessName()"]
    AS["方法: void setBusinessName(String businessName)"]
    AT["方法: String getFunctionName()"]
    AU["方法: void setFunctionName(String functionName)"]
    AV["方法: String getFunctionAuthor()"]
    AW["方法: void setFunctionAuthor(String functionAuthor)"]
    AX["方法: int getFormColNum()"]
    AY["方法: void setFormColNum(int formColNum)"]
    AZ["方法: String getGenType()"]
    BA["方法: void setGenType(String genType)"]
    BB["方法: String getGenPath()"]
    BC["方法: void setGenPath(String genPath)"]
    BD["方法: GenTableColumn getPkColumn()"]
    BE["方法: void setPkColumn(GenTableColumn pkColumn)"]
    BF["方法: GenTable getSubTable()"]
    BG["方法: void setSubTable(GenTable subTable)"]
    BH["方法: List<GenTableColumn> getColumns()"]
    BI["方法: void setColumns(List<GenTableColumn> columns)"]
    BJ["方法: String getOptions()"]
    BK["方法: void setOptions(String options)"]
    BL["方法: String getTreeCode()"]
    BM["方法: void setTreeCode(String treeCode)"]
    BN["方法: String getTreeParentCode()"]
    BO["方法: void setTreeParentCode(String treeParentCode)"]
    BP["方法: String getTreeName()"]
    BQ["方法: void setTreeName(String treeName)"]
    BR["方法: String getParentMenuId()"]
    BS["方法: void setParentMenuId(String parentMenuId)"]
    BT["方法: String getParentMenuName()"]
    BU["方法: void setParentMenuName(String parentMenuName)"]
    BV["方法: boolean isSub()"]
    BW["方法: static boolean isSub(String tplCategory)"]
    BX["方法: boolean isTree()"]
    BY["方法: static boolean isTree(String tplCategory)"]
    BZ["方法: boolean isCrud()"]
    CA["方法: static boolean isCrud(String tplCategory)"]
    CB["方法: boolean isSuperColumn(String javaField)"]
    CC["方法: static boolean isSuperColumn(String tplCategory, String javaField)"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H
    A --> I
    A --> J
    A --> K
    A --> L
    A --> M
    A --> N
    A --> O
    A --> P
    A --> Q
    A --> R
    A --> S
    A --> T
    A --> U
    A --> V
    A --> W
    A --> X
    A --> Y
    A --> Z
    A --> AA
    A --> AB
    A --> AC
    A --> AD
    A --> AE
    A --> AF
    A --> AG
    A --> AH
    A --> AI
    A --> AJ
    A --> AK
    A --> AL
    A --> AM
    A --> AN
    A --> AO
    A --> AP
    A --> AQ
    A --> AR
    A --> AS
    A --> AT
    A --> AU
    A --> AV
    A --> AW
    A --> AX
    A --> AY
    A --> AZ
    A --> BA
    A --> BB
    A --> BC
    A --> BD
    A --> BE
    A --> BF
    A --> BG
    A --> BH
    A --> BI
    A --> BJ
    A --> BK
    A --> BL
    A --> BM
    A --> BN
    A --> BO
    A --> BP
    A --> BQ
    A --> BR
    A --> BS
    A --> BT
    A --> BU
    A --> BV
    A --> BW
    A --> BX
    A --> BY
    A --> BZ
    A --> CA
    A --> CB
    A --> CC
```

这段代码定义了一个名为`GenTable`的类，该类继承自`BaseEntity`，包含了多个属性和方法。属性主要用于存储表的元数据信息，如表名、表描述、关联表信息等。方法则提供了对这些属性的访问和修改功能，以及一些用于判断表类型的静态方法。流程图展示了类`GenTable`的所有属性和方法，并清晰地表示了它们之间的关系。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| genPath | String | 私有字符串变量genPath。 |
| serialVersionUID = 1L | long | 定义了一个静态常量serialVersionUID，值为1L。 |
| tplCategory | String | 定义私有字符串变量tplCategory。 |
| genType | String | genType是私有字符串类型变量。 |
| tableComment | String | 表描述字段不能为空。 |
| tableId | Long | 表ID为长整型。 |
| tableName | String | 表名称字段不能为空。 |
| businessName | String | 业务名不能为空，使用注解验证。 |
| functionName | String | 功能名不能为空，使用注解确保非空验证。 |
| formColNum | int | 定义私有整型变量formColNum。 |
| subTableName | String | 定义了一个私有字符串变量subTableName。 |
| packageName | String | 生成包路径字段不能为空。 |
| functionAuthor | String | 代码定义了一个非空的作者字段。 |
| parentMenuId | String | 私有字符串变量parentMenuId。 |
| subTable | GenTable | 子表私有属性声明。 |
| treeCode | String | 定义私有字符串变量treeCode。 |
| className | String | 实体类名称字段不能为空，使用注解进行非空验证。 |
| pkColumn | GenTableColumn | 私有变量pkColumn，类型为GenTableColumn。 |
| treeName | String | 声明了一个私有字符串变量treeName。 |
| options | String | 私有字符串变量options定义。 |
| treeParentCode | String | 私有字符串变量treeParentCode用于存储父节点代码。 |
| moduleName | String | 生成模块名不能为空，定义私有字符串变量moduleName。 |
| columns | List<GenTableColumn> | `@Valid`验证`columns`列表中的`GenTableColumn`对象。 |
| parentMenuName | String | 定义私有字符串变量parentMenuName。 |
| subTableFkName | String | 子表外键名称字段声明。 |

### 方法列表 Method List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setBusinessName | void | 设置业务名称的方法。 |
| setSubTableFkName | void | 设置子表外键名称的方法。 |
| getSubTableName | String | 该方法返回子表名称。 |
| setSubTableName | void | 设置子表名称的方法。 |
| getFunctionAuthor | String | 该方法返回函数作者信息。 |
| getTableId | Long | 获取tableId的公共方法。 |
| getParentMenuId | String | 获取父菜单ID的方法。 |
| getFunctionName | String | 该方法返回函数名称。 |
| getClassName | String | 该方法返回类名。 |
| getGenPath | String | 获取生成路径的方法。 |
| getBusinessName | String | 获取业务名称的方法，返回businessName变量。 |
| getParentMenuName | String | 获取父菜单名称的方法。 |
| getTableName | String | 该方法返回表名。 |
| getGenType | String | 该方法返回genType变量的值。 |
| setParentMenuName | void | 设置父菜单名称的方法。 |
| setFunctionAuthor | void | 设置函数作者属性值。 |
| setTreeParentCode | void | 设置树形结构的父节点代码。 |
| setSubTable | void | 设置子表对象。 |
| setParentMenuId | void | 设置父菜单ID的方法。 |
| setPackageName | void | 设置类成员变量packageName的值。 |
| getTableComment | String | 获取表注释的字符串方法。 |
| setTreeName | void | 方法设置树名为传入参数值。 |
| setFormColNum | void | 该方法用于设置表单列数为指定值。 |
| getTreeParentCode | String | 获取树结构父节点代码的方法。 |
| getModuleName | String | 获取模块名称的方法，返回moduleName变量值。 |
| isTree | boolean | 检查对象是否为树结构。 |
| isCrud | boolean | 检查模板类别是否为CRUD类型。 |
| setPkColumn | void | 设置主键列的方法。 |
| isSuperColumn | boolean | 方法检查是否为超级列，调用内部方法判断。 |
| setOptions | void | 设置选项属性的Java方法。 |
| getSubTableFkName | String | 获取子表外键名称的方法。 |
| setTableComment | void | 该方法用于设置表注释，参数为字符串类型。 |
| isCrud | boolean | 判断当前模板类别是否为CRUD操作。 |
| isSub | boolean | 判断模板类别是否为子类别。 |
| setTableName | void | 该方法用于设置表名，将传入的字符串赋值给类的表名属性。 |
| getTreeCode | String | 获取treeCode的公共方法。 |
| getSubTable | GenTable | 获取子表的方法，返回subTable对象。 |
| setClassName | void | 设置类名的方法，将传入的className赋值给当前对象的className属性。 |
| getColumns | List<GenTableColumn> | 获取GenTableColumn类型的列数据列表。 |
| setModuleName | void | 设置模块名称的方法，将传入的moduleName赋值给当前对象的moduleName属性。 |
| getFormColNum | int | 获取表单列数的方法，返回整数类型。 |
| setGenType | void | 设置生成类型的方法，将参数genType赋值给类成员变量this.genType。 |
| setTableId | void | 设置表ID的方法，将传入的tableId赋值给当前对象的tableId属性。 |
| setTplCategory | void | 设置模板分类属性值。 |
| setGenPath | void | 设置生成路径的方法，用于赋值genPath变量。 |
| setColumns | void | 该方法用于设置表格列，接收列列表作为参数。 |
| getPkColumn | GenTableColumn | 获取主键列的方法，返回主键列对象。 |
| setTreeCode | void | 设置树编码的方法，将传入的treeCode赋值给当前对象的treeCode属性。 |
| isSub | boolean | 方法isSub返回this.tplCategory是否为子类别的布尔值。 |
| isSuperColumn | boolean | 判断字段是否为超级列，根据模板类别和Java字段匹配树实体或基础实体。 |
| getTreeName | String | 获取树名称的方法，返回变量treeName。 |
| getOptions | String | 获取options字符串的公共方法。 |
| getTplCategory | String | 获取模板类别的方法，返回tplCategory值。 |
| getPackageName | String | 获取包名的方法。 |
| isTree | boolean | 该方法判断tplCategory是否为树形模板类型。 |
| setFunctionName | void | 设置方法名，将传入值赋给类变量。 |




