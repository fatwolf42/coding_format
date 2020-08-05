# 目录
- [1 概述](#1-概述)
    - [1.1 目的](#11-目的)
    - [1.2 适用范围](#12-适用范围)
- [2 排版要求](#2-排版要求)
    - [2.1 程序块缩进](#21-程序块缩进)
    - [2.2 程序块之间空行](#22-程序块之间空行)
    - [2.3 长语句和长表达式](#23-长语句和长表达式)
    - [2.4 循环、判断等长表达式或语句](#24-循环判断等长表达式或语句)
    - [2.5 长参数](#25-长参数)
    - [2.6 短语句](#26-短语句)
    - [2.8 语句对齐](#28-语句对齐)
    - [2.9 函数、过程和结构等语句块](#29-函数过程和结构等语句块)
    - [2.10 程序块分界符](#210-程序块分界符)
    - [2.11 操作符前后空格](#211-操作符前后空格)
- [3 注释](#3-注释)
    - [3.1 有效注释量](#31-有效注释量)
    - [3.2 公司标识](#32-公司标识)
    - [3.5 函数头部说明](#35-函数头部说明)
    - [3.6 注释与代码一致](#36-注释与代码一致)
    - [3.7 注释内容](#37-注释内容)
    - [3.8 注释缩写](#38-注释缩写)
    - [3.9 注释位置](#39-注释位置)
    - [3.10 变量、常量注释](#310-变量常量注释)
    - [3.11 数据结构的注释](#311-数据结构的注释)
    - [3.12 全局变量](#312-全局变量)
    - [3.13 注释缩排](#313-注释缩排)
    - [3.14 注释与代码之间空行](#314-注释与代码之间空行)
    - [3.15 变量定义、分支语句](#315-变量定义分支语句)
    - [3.16 其他](#316-其他)
- [4 标识符命名](#4-标识符命名)
    - [4.1 命名清晰](#41-命名清晰)
    - [4.2 特殊命名需注释](#42-特殊命名需注释)
    - [4.3 命名风格保持一致](#43-命名风格保持一致)
    - [4.4 变量命名](#44-变量命名)
    - [4.5 命名规范与系统风格一致](#45-命名规范与系统风格一致)
    - [4.6 其他](#46-其他)
- [5 可读性](#5-可读性)
    - [5.1 运算符优先级](#51-运算符优先级)
    - [5.2 避免直接使用数字作为标识符](#52-避免直接使用数字作为标识符)
    - [5.3 其他](#53-其他)
- [6 变量、结构](#6-变量结构)
    - [6.1 公共变量](#61-公共变量)
    - [6.3 公共变量访问说明](#63-公共变量访问说明)
    - [6.4 公共变量赋值](#64-公共变量赋值)
    - [6.5 防止局部变量与公共变量同名。](#65-防止局部变量与公共变量同名)
    - [6.6 严禁使用未经初始化的变量作为右值。](#66-严禁使用未经初始化的变量作为右值)
    - [6.7 其他](#67-其他)
- [7 函数、过程](#7-函数过程)
    - [7.1 对所调用函数的错误返回码要仔细、全面地处理。](#71-对所调用函数的错误返回码要仔细全面地处理)
    - [7.2 明确函数功能，精确(而不是近似)地实现函数设计。](#72-明确函数功能精确而不是近似地实现函数设计)
    - [7.3 局部变量](#73-局部变量)
    - [7.4 全局变量](#74-全局变量)
    - [7.5 接口函数参数](#75-接口函数参数)
    - [7.6 其他](#76-其他)
- [8 可测性](#8-可测性)
    - [8.1 调测开关](#81-调测开关)
    - [8.2 打印信息](#82-打印信息)
    - [8.3 单元测试](#83-单元测试)
    - [8.4 集成测试](#84-集成测试)
    - [8.5 断言使用](#85-断言使用)
    - [8.6 设置与取消有关测试手段时，不能影响软件功能功能](#86-设置与取消有关测试手段时不能影响软件功能功能)
    - [8.7 版本维护](#87-版本维护)
    - [8.8 其他](#88-其他)
- [9 程序效率](#9-程序效率)
    - [9.1 编程时要经常注意代码的效率。](#91-编程时要经常注意代码的效率)
    - [9.2 提高代码效率](#92-提高代码效率)
    - [9.3 全局效率高于局部效率](#93-全局效率高于局部效率)
    - [9.4 提高代码空间效率](#94-提高代码空间效率)
    - [9.5 循环体内工作量最小化](#95-循环体内工作量最小化)
    - [9.6 其他](#96-其他)
- [10 质量保证](#10-质量保证)
    - [10.1 在软件设计过程中构筑软件质量。](#101-在软件设计过程中构筑软件质量)
    - [10.2 代码质量保证优先原则](#102-代码质量保证优先原则)
    - [10.3 只引用属于自己的存贮空间。](#103-只引用属于自己的存贮空间)
    - [10.4 防止引用已经释放的内存空间。](#104-防止引用已经释放的内存空间)
    - [10.5 内存及时释放](#105-内存及时释放)
    - [10.6 文件句柄及时关闭](#106-文件句柄及时关闭)
    - [10.7 防止内存操作越界](#107-防止内存操作越界)
    - [10.8 认真处理程序所能遇到的各种出错情况](#108-认真处理程序所能遇到的各种出错情况)
    - [10.9 初始化变量](#109-初始化变量)
    - [10.10 数据一致性检查](#1010-数据一致性检查)
    - [10.11 严禁随意更改其它模块或系统的有关设置和配置](#1011-严禁随意更改其它模块或系统的有关设置和配置)
    - [10.12 不能随意改变与其它模块的接口](#1012-不能随意改变与其它模块的接口)
    - [10.13 系统接口](#1013-系统接口)
    - [10.14 编程时，要防止差1错误](#1014-编程时，要防止差1错误)
    - [10.15 操作符检查](#1015-操作符检查)
    - [10.16 分支语句写完整](#1016-分支语句写完整)
    - [10.17 使用return语句](#1017-使用return语句)
    - [10.18 不要滥用goto语句](#1018-不要滥用goto语句)
    - [10.19 其他](#1019-其他)
- [11 代码编辑、编译、审查](#11-代码编辑编译审查)
    - [11.1 打开编译器的所有告警开关对程序进行编译](#111-打开编译器的所有告警开关对程序进行编译)
    - [11.2 在产品软件(项目组)中，要统一编译开关选项](#112-在产品软件项目组中要统一编译开关选项)
    - [11.3 通过代码走读及审查方式对代码进行检查。](#113-通过代码走读及审查方式对代码进行检查)
    - [11.4 测试部测试产品之前，应对代码进行抽查及评审](#114-测试部测试产品之前应对代码进行抽查及评审)
    - [11.5 其他](#115-其他)
- [12 代码测试、维护](#12-代码测试维护)
    - [12.1 单元测试要求至少达到语句覆盖](#121-单元测试要求至少达到语句覆盖)
    - [12.2 单元测试开始要跟踪每一条语句，并观察数据流及变量的变化](#122-单元测试开始要跟踪每一条语句并观察数据流及变量的变化)
    - [12.3 清理、整理或优化后的代码要经过审查及测试。](#123-清理整理或优化后的代码要经过审查及测试)
    - [12.4 代码版本升级要经过严格测试](#124-代码版本升级要经过严格测试)
    - [12.5 使用工具软件对代码版本进行维护](#125-使用工具软件对代码版本进行维护)
    - [12.6 正式版本上软件的任何修改都应有详细的文档记录](#126-正式版本上软件的任何修改都应有详细的文档记录)
    - [12.7 其他](#127-其他)
- [13 宏](#13-宏)
    - [13.1 用宏定义表达式时，要使用完备的括号](#131-用宏定义表达式时要使用完备的括号)
    - [13.2 将宏所定义的多条表达式放在大括号中](#132-将宏所定义的多条表达式放在大括号中)
    - [13.3 使用宏时，不允许参数发生变化](#133-使用宏时不允许参数发生变化)


1 概述
========

1.1 目的
--------
为形成公司统一的C++编码风格，以保障公司项目代码的易维护性和编码安全性，特制定本规范。

1.2 适用范围
--------
本标准适用于公司所有使用C++作为开发语言的软件产品。原则上，C++开发遵循本规范说明，特殊情况可例外，但需跟技术架构委员会说明原因。

2 排版要求
========
2.1 程序块缩进
--------
程序块要采用缩进风格编写，缩进的空格数为 4 个。 说明:对于由开发工具自动生成的代码可以有不一致。

2.2 程序块之间空行
--------
相对独立的程序块之间、变量说明之后必须加空行。

示例:如下例子不符合规范。 

    if (!valid_ni(ni)) {
        ... // program code
    }
    repssn_ind = ssn_data[index].repssn_index;
    repssn_ni = ssn_data[index].ni;

应如下书写

    if (!valid_ni(ni)) 
    {
        ... // program code
    }


    repssn_ind = ssn_data[index].repssn_index;
    repssn_ni = ssn_data[index].ni;

2.3 长语句和长表达式
--------
较长的语句(>80字符)要分成多行书写，长表达式要在低优先级操作符处划分新行，操作符放在新行之首，划分出的新行要进行适当的缩进，使排版整齐，语句可读。
示例:

    perm_count_msg.head.len = NO7_TO_STAT_PERM_COUNT_LEN
                            + STAT_SIZE_PER_FRAM * sizeof( _UL );


    act_task_table[frame_id * STAT_TASK_CHECK_NUMBER + index].occupied
                            = stat_poi[index].occupied;


    act_task_table[taskno].duration_true_or_false
                            = SYS_get_sccp_statistic_state( stat_item );


    report_or_not_flag = ((taskno < MAX_ACT_TASK_NUMBER)
                            && (n7stat_stat_item_valid (stat_item))
                                && (act_task_table[taskno].result_data != 0));

2.4 循环、判断等长表达式或语句
--------
循环、判断等语句中若有较长的表达式或语句，则要进行适应的划分，长表达式要在低优先级操作符 处划分新行，操作符放在新行之首。

示例:

    if ((taskno < max_act_task_number)
        && (n7stat_stat_item_valid (stat_item)))
    {
        ... // program code
    }

    for (i = 0, j = 0; (i < BufferKeyword[word_index].word_length)
                        && (j < NewKeyword.word_length); i++, j++)
    {
        ... // program code
    }

    for (i = 0, j = 0;
        (i < first_word_length) && (j < second_word_length);
        i++, j++)
    {
        ... // program code
    }

2.5 长参数
--------
若函数或过程中的参数较长，则要进行适当的划分。
示例:

    n7stat_str_compare((BYTE *) & stat_object,
                        (BYTE *) & (act_task_table[taskno].stat_object),
                        sizeof (_STAT_OBJECT));


    n7stat_flash_act_duration( stat_item, frame_id *STAT_TASK_CHECK_NUMBER
                                    + index, stat_object );

2.6 短语句
--------
不允许把多个短语句写在一行中，即一行只写一条语句。

示例:如下例子不符合规范。 
    
    rect.length = 0; rect.width = 0;

应如下书写

    rect.length = 0;
    rect.width = 0;

2.7 条件、循环语句
--------
``if、for、do、while、case、switch、default``等语句自占一行，且``if、for、do、while``等语句的执行语句部分无论多少都要加括号``{}``。

示例:如下例子不符合规范。 

    if (pUserCR == NULL) return;

应如下书写:

    if (pUserCR == NULL)
    {
        return;
    }

2.8 语句对齐
--------
对齐只使用空格键，不使用``TAB``键。
说明:以免用不同的编辑器阅读程序时，因``TAB``键所设置的空格数目不同而造成程序布局不整齐，不要使用 BC 作为编辑器合版本，因为 BC 会自动将 8 个空格变为一个 TAB 键，因此使用 BC 合入的版本大多会将缩进变乱。

2.9 函数、过程和结构等语句块
--------
函数或过程的开始、结构的定义及循环、判断等语句中的代码都要采用缩进风格，``case``语句下的情 况处理语句也要遵从语句缩进要求。

2.10 程序块分界符
--------
程序块的分界符(如C/C++语言的大括号`{`和`}`)应各独占一行并且位于同一列，同时与引用 它们的语句左对齐。在函数体的开始、类的定义、结构的定义、枚举的定义以及`if、for、do、while、 switch、case`语句中的程序都要采用如上的缩进方式。

示例:如下例子不符合规范。 
 
    for (...) {
        ... // program code
    }

    if (...)
        {
        ... // program code
        }


    void example_fun( void )
        {
        ... // program code
        }

应如下书写。

    for (...) {
        ... // program code
    }

    if (...)
    {
        ... // program code
    }


    void example_fun( void )
    {
        ... // program code
    }

2.11 操作符前后空格
--------
在两个以上的关键字、变量、常量进行对等操作时，它们之间的操作符之前、之后或者前后要加空格; 进行非对等操作时，如果是关系密切的立即操作符(如`->`)，后不应加空格。

说明:采用这种松散方式编写代码的目的是使代码更加清晰。 由于留空格所产生的清晰性是相对的，所以，在已经非常清晰的语句中没有必要再留空格，如果语句 已足够清晰则括号内侧(即左括号后面和右括号前面)不需要加空格，多重括号间不必加空格，因为 在 C/C++语言中括号已经是最清晰的标志了。 在长语句中，如果需要加的空格非常多，那么应该保持整体清晰，而在局部不加空格。给操作符留空格时不要连续留两个以上空格。

示例:
1. 逗号、分号只在后面加空格。

        int a, b, c;

2. 比较操作符, 赋值操作符"="、 "+="，算术操作符"+"、"%"，逻辑操作符"&&"、"&"，位域 操作符"<<"、"^"等双目操作符的前后加空格。

        if (current_time >= MAX_TIME_VALUE)
        a = b + c;
        a *= 2;
        a = b ^ 2;

3. `"!"、"~"、"++"、"--"、"&"`(地址运算符)等单目操作符前后不加空格。 

        *p = 'a'; // 内容操作"*"与内容之间
        flag = !isEmpty; // 非操作"!"与内容之间
        p = &mem; // 地址操作"&" 与内容之间
        i++; // "++","--"与内容之间

4. `"->"、"."`前后不加空格。

        p->id = pid; // "->"指针前后不加空格

5.  if、for、while、switch等与后面的括号间应加空格，使if等关键字更为突出、明显。 

        if (a >= b && c > d)

2.12 其他
--------
一行程序以小于 80 字符为宜，不要写得过长。


3 注释
========
3.1 有效注释量
--------
一般情况下，源程序有效注释量必须在 **20%** 以上。 说明:注释的原则是有助于对程序的阅读理解，在该加的地方都加了，注释不宜太多也不能太少，注释语言必须准确、易懂、简洁。

3.2 公司标识
--------
在头文件中加入公司标识。

示例如下: 

    /*
    /* Copyright (c) 1996-1998 XXXXXX Company
    */ 版权所有 1996-1998 */
    /* /*
    xxxxxxxx
    */
    /* PROPRIETARY RIGHTS of XXXXXX Company are involved in the
    */
    /*  subject matter of this material. All manufacturing, reproduction, use,*/

    /*  and sales rights pertaining to this subject matter are governed by the */


    */
    /* license agreement. The recipient of this software implicitly accepts */ /* the terms of the
    license.
    */
    /* 本软件文档资料是 xxx 公司的资产,任何人士阅读和使用本资料必须获得 */ /* 相应的书面授权,承担保密责任和接受相应的法律约
    束. */
    /*
    */
    /**************************************************************************/

3.3 说明性文件
--------
说明性文件(如头文件.h 文件、.inc 文件、.def 文件、编译说明文件.cfg 等)头部应进行注释，注释必须列出:版权说明、版本号、生成日期、作者、内容、功能、与其它文件的关系、修改日志等，头文件的注释中还应有函数功能简要说明。

示例:下面这段头文件的头注释比较标准，当然，并不局限于此格式，但上述信息建议要包含在内。

    /************************************************* Copyright (C), 1996-1998, xxxxx. Co., Ltd.
    // 文件名
    Version: Date: // 作者、版本及完成日期
    // 用于详细说明此程序文件完成的主要功能，与其他模块 // 或函数的接口，输出值、取值范围、含义及参数间的控 // 制、顺序、独立或依赖等关系
    1. ....
    History: // 修改历史记录列表，每条修改记录应包括修改日期、修改
    // 者及修改内容简述
    File name: Author: Description:
    Others:
    Function List: // 主要函数列表，每条记录应包括函数名及功能简要说明
    // 其它内容的说明
     1. Date: Author:
     Modification: 2. ...
    *************************************************/

3.4 源文件头
--------
源文件头部应进行注释，列出:版权说明、版本号、生成日期、作者、模块目的/功能、主要函数及其功能、修改日志等。

示例:下面这段源文件的头注释比较标准，当然，并不局限于此格式，但上述信息建议要包含在内。

    /************************************************************ Copyright (C), 1988-1999, Xxxxxx Tech. Co., Ltd.
    FileName: test.cpp
     Author:    Version:    Date:
    Description:        // 模块描述
    Version:            // 版本信息
    Function List:      // 主要函数及其功能
     1. -------
    History:        // 历史修改记录
    <author>  <time>        <version >        <desc>
    David   96/10/12        1.0             build this moudle
    ***********************************************************/

说明:`Description` 一项描述本文件的内容、功能、内部各部分之间的关系及本文件与其它文件关 系等。`History` 是修改历史记录列表，每条修改记录应包括修改日期、修改者及修改内容简述。

3.5 函数头部说明
--------
函数头部应进行注释，列出:函数的目的/功能、输入参数、输出参数、返回值、调用关系(函数、表)等。
示例:下面这段函数的注释比较标准，当然，并不局限于此格式，但上述信息建议要包含在内。

    /*************************************************
    Function:       // 函数名称
    Description:    // 函数功能、性能等的描述
    Calls:          // 被本函数调用的函数清单
    Called By:      // 调用本函数的函数清单
    Table Accessed: // 被访问的表(此项仅对于牵扯到数据库操作的程序)
    Table Updated:  // 被修改的表(此项仅对于牵扯到数据库操作的程序)
    Input:          // 输入参数说明，包括每个参数的作
                    // 用、取值说明及参数间关系。
    Output:         // 对输出参数的说明。
    Return:         // 函数返回值的说明
    Others:         // 其它说明
    *************************************************/

3.6 注释与代码一致
--------
边写代码边注释，修改代码同时修改相应的注释，以保证注释与代码的一致性。不再有用的注释要删除。

3.7 注释内容
--------
注释的内容要清楚、明了，含义准确，防止注释二义性。

说明:错误的注释不但无益反而有害。 

3.8 注释缩写
--------
避免在注释中使用缩写。

说明:在使用缩写时或之前，应对缩写进行必要的说明。
 
3.9 注释位置
--------
注释应与其描述的代码相近，对代码的注释应放在其上方或右方(对单条语句的注释)相邻位置，不可放在下面，如放于上方则需与其上面的代码用空行隔开。

示例:如下例子不符合规范。
- 例 1:

        /* get replicate sub system index and net indicator */

        repssn_ind = ssn_data[index].repssn_index;
        repssn_ni = ssn_data[index].ni;

- 例 2:

        repssn_ind = ssn_data[index].repssn_index;
        repssn_ni = ssn_data[index].ni;
        /* get replicate sub system index and net indicator */
        应如下书写

        /* get replicate sub system index and net indicator */
        repssn_ind = ssn_data[index].repssn_index;
        repssn_ni = ssn_data[index].ni;

3.10 变量、常量注释
--------
对于所有有物理含义的变量、常量，如果其命名不是充分自注释的，在声明时都必须加以注释，说明其物理含义。变量、常量、宏的注释应放在其上方相邻位置或右方。

示例:

    /* active statistic task number */ #define MAX_ACT_TASK_NUMBER 1000
    #define MAX_ACT_TASK_NUMBER 1000 /* active statistic task number */

3.11 数据结构的注释
--------
数据结构声明(包括数组、结构、类、枚举等)，如果其命名不是充分自注释的，必须加以注释。对数据结构的注释应放在其上方相邻位置，不可放在下面;对结构中的每个域的注释放在此域的右方。

示例:可按如下形式说明枚举/数据/联合结构。

    /* sccp interface with sccp user primitive message name */
    enum SCCP_USER_PRIMITIVE
    {
        N_UNITDATA_IND, /* sccp notify sccp user unit data come */
        N_NOTICE_IND,   /* sccp notify user the No.7 network can not */
                        /* transmission this message */
        N_UNITDATA_REQ, /* sccp user's unit data transmission request*/
    };

3.12 全局变量
--------
全局变量要有较详细的注释，包括对其功能、取值范围、哪些函数或过程存取它以及存取时注意事项等的说明。

示例:

    /* The ErrorCode when SCCP translate */
    /* Global Title failure, as follows */  // 变量作用、含义
    /* 0 - SUCCESS 1 - GT Table error */
    /* 2 - GT error Others - no use */      // 变量取值范围
    /* only function SCCPTranslate() in */
    /* this modual can modify it, and other */
    /* module can visit it through call */
    /* the function GetGTTransErrorCode() */    // 使用方法
    BYTE g_GTTranErrorCode;

3.13 注释缩排
--------
注释与所描述内容进行同样的缩排。

说明:可使程序排版整齐，并方便注释的阅读与理解。 示例:如下例子，排版不整齐，阅读稍感不方便。

 

    void example_fun( void )
    {
        /* code one comments */
        CodeBlock One


            /* code two comments */
            CodeBlock Two
    }

应改为如下布局。

    void example_fun( void ) {
        /* code one comments */
        CodeBlock One

        /* code two comments */
        CodeBlock Two
    }

3.14 注释与代码之间空行
--------
将注释与其上面的代码用空行隔开。

示例:如下例子，显得代码过于紧凑。

    /* code one comments */
    program code one
    /* code two comments */
    program code two

应如下书写

    /* code one comments */
    program code one

    /* code two comments */
    program code two

3.15 变量定义、分支语句
--------
对变量的定义和分支语句(条件分支、循环语句等)必须编写注释。

说明:这些语句往往是程序实现某一特定功能的关键，对于维护人员来说，良好的注释帮助更好的理 解程序，有时甚至优于看设计文档。

示例(注意`ProcessCFW_B`部分):

    case CMD_UP:
        ProcessUp();
        break;

    case CMD_DOWN:
        ProcessDown();
        break;

    case CMD_FWD:
        ProcessFwd();

        if (...) {
            ...
            break;
        }
        else {
            ProcessCFW_B(); // now jump into case CMD_A
        }


    case CMD_A:
        ProcessA();
        break;

    case CMD_B:
        ProcessB();
        break;

    case CMD_C:
        ProcessC();
        break;

    case CMD_D:
        ProcessD();
        break;
    ...

3.16 其他
--------
### 3.16.1 避免在一行代码或表达式的中间插入注释。 

说明:除非必要，不应在代码或表达中间插入注释，否则容易使代码可理解性变差。



### 3.16.2 通过对函数或过程、变量、结构等正确的命名以及合理地组织代码的结构， 使代码成为自注释的。

说明:清晰准确的函数、变量等的命名，可增加代码可读性，并减少不必要的注释。



### 3.16.3 在代码的功能、意图层次上进行注释，提供有用、额外的信息。

说明:注释的目的是解释代码的目的、功能和采用的方法，提供代码以外的信息，帮助读者理解代码， 防止没必要的重复注释信息。

示例:如下注释意义不大。

        /* if receive_flag is TRUE */
        if (receive_flag)

而如下的注释则给出了额外有用的信息。 
     
        /* if mtp receive a message from links */
        if (receive_flag)

### 3.16.4 在程序块的结束行右方加注释标记，以表明某程序块的结束。

说明:当代码段较长，特别是多重嵌套时，这样做可以使代码更清晰，更便于阅读。 示例:参见如下例子。

        if (...)
        {
            // program code

            while (index < MAX_INDEX) {
                // program code
            } /* end of while (index < MAX_INDEX) */ // 指明该条 while 语句结束
        } /* end of if (...)*/ // 指明是哪条 if 语句结束


### 3.16.5 注释格式尽量统一，建议使用`/* ...... */`。

### 3.16.6 注释应考虑程序易读及外观排版的因素，使用的语言若是中、英兼有的， 建议多使用中文，除非能用非常流利准确的英文表达。

说明:注释语言不统一，影响程序易读性和外观排版，出于对维护人员的考虑，建议使用 *中文* 。


4 标识符命名
========
4.1 命名清晰
--------
标识符的命名要清晰、明了，有明确含义，同时使用完整的单词或大家基本可以理解的缩写，避免使人产生误解。

说明:较短的单词可通过去掉“元音”形成缩写;较长的单词可取单词的头几个字母形成缩写;一些单词有大家公认的缩写。

示例:如下单词的缩写能够被大家基本认可。 

    temp 可缩写为 tmp ;

    flag 可缩写为 flg ;

    statistic 可缩写为 stat ;

    increment 可缩写为 inc ;

    message 可缩写为 msg ;

4.2 特殊命名需注释
--------
命名中若使用特殊约定或缩写，则要有注释说明。

说明:应该在源文件的开始之处，对文件中所使用的缩写或约定，特别是特殊的缩写，进行必要的注释说明。

4.3 命名风格保持一致
--------
自己特有的命名风格，要自始至终保持一致，不可来回变化。

说明:个人的命名风格，在符合所在项目组或产品组的命名规则的前提下，才可使用。(即命名规则中没有规定到的地方才可有个人命名风格)。

4.4 变量命名
--------
对于变量命名，禁止取单个字符(如 `i、j、k...`)，建议除了要有具体含义外，还能表明其变量类型、 数据类型等，但 `i、j、k `作局部循环变量是允许的。

说明:变量，尤其是局部变量，如果用单个字符表示，很容易敲错(如` i` 写成` j`)，而编译时又检查不出来，有可能为了这个小小的错误而花费大量的查错时间。 示例:下面所示的局部变量名的定义方法可以借鉴。

    int liv_Width

其变量名解释如下:

    l 局部变量(Local) (其它:g 全局变量(Global)...)

    i 数据类型(Interger)


    v 变量(Variable) (其它:c 

    Width 变量含义

这样可以防止局部变量与全局变量重名。 

4.5 命名规范与系统风格一致
--------
命名规范必须与所使用的系统风格保持一致，并在同一项目中统一，比如采用 UNIX 的全小写加下划 线的风格或大小写混排的方式，不要使用大小写与下划线混排的方式，用作特殊标识如标识成员变量或全 局变量的` m_和 g_`，其后加上大小写混排的方式是允许的。

示例: `Add_User` 不允许，`add_user、AddUser、m_AddUser` 允许。 

4.6 其他
---------
### 4.6.1 除非必要，不要用数字或较奇怪的字符来定义标识符。

示例:如下命名，使人产生疑惑。 

    #define _EXAMPLE_0_TEST_
    #define _EXAMPLE_1_TEST_
    void set_sls00( BYTE sls );

应改为有意义的单词命名

    #define _EXAMPLE_UNIT_TEST_
    #define _EXAMPLE_ASSERT_TEST_
    void set_udt_msg_sls( BYTE sls );

### 4.6.2 在同一软件产品内，应规划好接口部分标识符(变量、结构、函数及常 量)的命名，防止编译、链接时产生冲突。

说明:对接口部分的标识符应该有更严格限制，防止冲突。如可规定接口部分的变量与常量之前加上 “模块”标识等。



### 4.6.3 用正确的反义词组命名具有互斥意义的变量或相反动作的函数等。

说明:下面是一些在软件中常用的反义词组。 

    add / remove
    begin / end
    insert / delete
    first / last
    increment / decrement
    create / destroy 
    get / release 
    put / get
    add / delete
    min / max
    next / previous
    send / receive
    cut / paste 
    lock / unlock 
    old / new 
    source / target 
    source / destination 
    up / down
    open / close 
    start / stop 
    show / hide

示例:

    int min_sum;
    int max_sum;
    int add_user( BYTE *user_name ); int delete_user( BYTE *user_name );

### 4.6.4 除了编译开关/头文件等特殊应用，应避免使用`_EXAMPLE_TEST_`之类以下 划线开始和结尾的定义。

5 可读性
========
5.1 运算符优先级
--------
注意运算符的优先级，并用括号明确表达式的操作顺序，避免使用默认优先级。

说明:防止阅读程序时产生误解，防止因默认的优先级与设计思想不符而导致程序出错。

示例:下列语句中的表达式

    word = (high << 8) | low      (1)
    if ((a | b) && (a & c))     (2)
    if ((a | b) < (c & d))       (3)

如果书写为

    high << 8 | low
    a | b && a & c
    a | b < c & d

由于

    high << 8 | low = ( high << 8) | low,
    a | b && a & c = (a | b) && (a & c)，

(1)(2)不会出错，但语句不易理解;
 
    a | b < c & d = a | (b < c) & d，

(3)造成了判断条件出错。

5.2 避免直接使用数字作为标识符
--------
避免使用不易理解的数字，用有意义的标识来替代。涉及物理状态或者含有物理意义的常量，不应直 接使用数字，必须用有意义的枚举或宏来代替。

示例:如下的程序可读性差。 

    if (Trunk[index].trunk_state == 0) {
        Trunk[index].trunk_state = 1;
        ... // program code
    }

应改为如下形式。

    #define TRUNK_IDLE 0
    #define TRUNK_BUSY 1

    if (Trunk[index].trunk_state == TRUNK_IDLE) {
        Trunk[index].trunk_state = TRUNK_BUSY;
        ... // program code
    }

5.3 其他
--------
### 5.3.1 源程序中关系较为紧密的代码应尽可能相邻。

说明:便于程序阅读和查找。

示例:以下代码布局不太合理。 

    rect.length = 10;
    char_poi = str;
    rect.width = 5;

若按如下形式书写，可能更清晰一些。 

    rect.length = 10;
    rect.width = 5; // 矩形的长与宽关系较密切，放在一起。
    char_poi = str;

### 5.3.2 不要使用难懂的技巧性很高的语句，除非很有必要时。

说明:高技巧语句不等于高效率的程序，实际上程序的效率关键在于算法。 示例:如下表达式，考虑不周就可能出问题，也较难理解。

    stat_poi++ += 1;
    ++stat_poi += 1;


应分别改为如下。

    stat_poi += 1;
    stat_poi++;     // 此二语句功能相当于“stat_poi ++ += 1; ”
    ++stat_poi;
    stat_poi += 1; // 此二语句功能相当于“++stat_poi += 1;
