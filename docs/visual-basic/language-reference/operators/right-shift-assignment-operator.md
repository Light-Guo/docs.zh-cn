---
title: '>>= 运算符'
ms.date: 07/20/2015
f1_keywords:
- vb.>>=
helpviewer_keywords:
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- operator >>= [Visual Basic]
- compound assignment statements [Visual Basic]
- '>>= operator [Visual Basic]'
ms.assetid: 2bcd9abb-7a8c-4229-b75d-8816ff1dc700
ms.openlocfilehash: cad021c7730782d6233c60841483df7173308dc1
ms.sourcegitcommit: 17ee6605e01ef32506f8fdc686954244ba6911de
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2019
ms.locfileid: "74351999"
---
# <a name="-operator-visual-basic"></a>> > = 运算符（Visual Basic）
对变量或属性的值执行算术右移位，并将结果赋回给变量或属性。  
  
## <a name="syntax"></a>语法  
  
```vb  
variableorproperty >>= amount  
```  
  
## <a name="parts"></a>部件  
 `variableorproperty`  
 必需。 整数类型（`SByte`、`Byte`、`Short`、`UShort`、`Integer`、`UInteger`、`Long`或 `ULong`）的变量或属性。  
  
 `amount`  
 必需。 扩大到 `Integer`的数据类型的数值表达式。  
  
## <a name="remarks"></a>备注  
 `>>=` 运算符左侧的元素可以是简单的标量变量、属性或数组的元素。 变量或属性不能是[只读](../../../visual-basic/language-reference/modifiers/readonly.md)的。  
  
 `>>=` 运算符首先对变量或属性的值执行算术右移位运算。 然后，运算符将该操作的结果赋给变量或属性。  
  
 算术移位不是循环的，这意味着，不会在另一端重新引入结果的末尾以外的位。 在算术右移位时，将丢弃超出最右位位置的位，并将最左侧的位传播到左端空出的位位置。 这意味着，如果 `variableorproperty` 具有负值，则空出位置将设置为1。 如果 `variableorproperty` 为正值，或者其数据类型为无符号类型，则空出位置将设置为零。  
  
## <a name="overloading"></a>重载  
 [> > 运算符](../../../visual-basic/language-reference/operators/right-shift-operator.md)可*重载*，这意味着当操作数具有该类或结构的类型时，该类或结构可以重新定义其行为。 重载 `>>` 运算符会影响 `>>=` 运算符的行为。 如果你的代码在重载 `>>`的类或结构上使用 `>>=`，请确保了解其重新定义的行为。 有关更多信息，请参见 [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)。  
  
## <a name="example"></a>示例  
 下面的示例使用 `>>=` 运算符将 `Integer` 变量的位模式向右移动指定的量，并将结果赋给该变量。  
  
 [!code-vb[VbVbalrOperators#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#15)]  
  
## <a name="see-also"></a>另请参阅

- [>> 运算符](../../../visual-basic/language-reference/operators/right-shift-operator.md)
- [赋值运算符](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [移位运算符](../../../visual-basic/language-reference/operators/bit-shift-operators.md)
- [Visual Basic 中的运算符优先级](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [按功能列出的运算符](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [语句](../../../visual-basic/programming-guide/language-features/statements.md)
