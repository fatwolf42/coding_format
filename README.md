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
