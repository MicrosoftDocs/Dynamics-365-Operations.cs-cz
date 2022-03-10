---
title: Nastavení účetních profilů dlouhodobého majetku
description: Tento postup ukazuje, jak nastavit účetní profily dlouhodobého majetku.
author: moaamer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0006c9588a22d720687e7aceb49acc756b83e1
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883761"
---
# <a name="set-up-fixed-asset-posting-profiles"></a>Nastavení účetních profilů dlouhodobého majetku

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje, jak nastavit účetní profily dlouhodobého majetku. Příklady uvedené v tématu jsou určeny pro základní účetní profil, i když účetní profily je nutné vytvořit pro vaši konkrétní účtovou osnovu a požadavky na finanční výkazy.

1. V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Nastavení > Účetní profily dlouhodobého majetku**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Účetní profil**.
4. Zadejte hodnotu do pole **Popis**. Musíte vytvořit zaúčtovací profil pro každý typ transakce dlouhodobého majetku, který chcete použít při práci s dlouhodobým majetkem. Tento průvodce úkolem se spustí s typem Transakce pořízení.  
5. Na panelu nástrojů klikněte na tlačítko **Přidat**.
6. V poli **Kniha** zadejte nebo vyberte hodnotu. Pole **Seskupení** umožňuje definovat účetní profil pro tabulku (jeden účet pro každý dlouhodobý majetek) nebo skupinu (jeden účet pro každou skupinu dlouhodobého majetku). Pro tohoto průvodce záznamem úloh ponecháme nastavenou hodnotu „Vše“ a použijeme tak veškerý dlouhodobý majetek se zadanou knihou.  
7. Zadejte požadované hodnoty do pole **Hlavní účet**. Pro pořízení zadejte protiúčet, nebo ponechejte pole prázdné a nechte je vyplnit pro určitou transakci.    
8. V rozevírací nabídce na pevné záložce **Účty hlavní knihy** vyberte možnost Oprava pořizovací ceny. Pro úpravu transakcí opravy pořizovací ceny použijeme stejné účty, které byly použity pro transakce pořízení.  
9. Klikněte na tlačítko **Přidat**.
10. V poli **Kniha** zadejte nebo vyberte hodnotu.
11. Zadejte požadované hodnoty do pole **Hlavní účet**. Pro opravy pořizovací ceny zadejte protiúčet, nebo ponechejte pole prázdné a nechte je vyplnit pro určitou transakci.    
12. V rozevírací nabídce na pevné záložce **Účty hlavní knihy** vyberte možnost Odpisy.
13. Klikněte na tlačítko **Přidat**.
14. V poli **Kniha** zadejte nebo vyberte hodnotu.
15. Zadejte požadované hodnoty do pole **Hlavní účet**.
16. Zadejte požadované hodnoty do pole **Protiúčet**.
17. V rozevírací nabídce na pevné záložce **Účty hlavní knihy** vyberte možnost Oprava odpisu. Pro úpravu transakcí odpisů použijeme stejné účty, které byly použity pro transakce odpisů.  
18. Klikněte na tlačítko **Přidat**.
19. V poli **Kniha** zadejte nebo vyberte hodnotu.
20. Zadejte požadované hodnoty do pole **Hlavní účet**.
21. Zadejte požadované hodnoty do pole **Protiúčet**.
22. V rozevírací nabídce na pevné záložce **Účty hlavní knihy** vyberte možnost Vyřazení – odprodej.
23. Klikněte na tlačítko **Přidat**.
24. V poli **Kniha** zadejte nebo vyberte hodnotu.
25. Zadejte požadované hodnoty do pole **Hlavní účet**. Pro vyřazení zadejte protiúčet, nebo ponechejte pole prázdné a nechte je vyplnit pro určitou transakci.  
26. V rozevírací nabídce na pevné záložce **Účty hlavní knihy** vyberte možnost Vyřazení – likvidace. Použijte stejné účty pro Vyřazení – odprodej a Vyřazení – likvidace.  
27. Klikněte na tlačítko **Přidat**.
28. V poli **Kniha** zadejte nebo vyberte hodnotu.
29. Zadejte požadované hodnoty do pole **Hlavní účet**. Pro vyřazení zadejte protiúčet, nebo ponechejte pole prázdné a nechte je vyplnit pro určitou transakci.  
30. Rozbalte pevnou záložku **Vyřazení**. Nastavte účetní profily pro vyřazení prodeje i odpadu.  Začneme s transakcemi zaměřenými na odprodej po vyřazení.  
31. Klikněte na tlačítko **Přidat**.
32. V poli **Kniha** zadejte nebo vyberte hodnotu.
33. V poli **Zaúčtovat hodnotu** vyberte Pořizovací hodnota.
    * Pořizovací hodnota se zaměřuje na pořízení a opravu pořizovací ceny pro všechny roky. Můžete také definovat účty pro tyto typy transakcí samostatně.  
    * Můžete nastavit proces vyřazení tak, aby používal různé účty v závislosti na tom, zda je výsledkem odpisu zisk nebo ztráta. Nastavíme hodnotu prodeje na „Vše“ a použijeme tak stejné účty pro všechny typy vyřazení.  
34. Zadejte požadované hodnoty do pole **Hlavní účet**.
35. Zadejte požadované hodnoty do pole **Protiúčet**.
36. Klikněte na tlačítko **Přidat**.
37. V poli **Kniha** zadejte nebo vyberte hodnotu.
38. V poli **Zaúčtovat hodnotu** vyberte hodnotu Odpis (předchozí roky).  
38. Zadejte požadované hodnoty do pole **Hlavní účet**.
39. Zadejte požadované hodnoty do pole **Protiúčet**.
40. Klikněte na tlačítko **Přidat**.
41. V poli **Kniha** zadejte nebo vyberte hodnotu.
42. V poli **Zaúčtovat hodnotu** vyberte hodnotu Odpis (tento rok).
43. Zadejte požadované hodnoty do pole **Hlavní účet**.
44. Zadejte požadované hodnoty do pole **Protiúčet**.
45. Klikněte na tlačítko **Přidat**.
46. V poli **Kniha** zadejte nebo vyberte hodnotu.
47. V poli **Zaúčtovat hodnotu** vyberte hodnotu Opravy odpisů (předchozí roky).
48. Zadejte požadované hodnoty do pole **Hlavní účet**.
49. Zadejte požadované hodnoty do pole **Protiúčet**.
50. Klikněte na tlačítko **Přidat**.
51. V poli **Kniha** zadejte nebo vyberte hodnotu.
52. V poli **Zaúčtovat hodnotu** vyberte hodnotu Opravy odpisů (tento rok).
53. Zadejte požadované hodnoty do pole **Hlavní účet**.
54. Zadejte požadované hodnoty do pole **Protiúčet**.
55. Klikněte na tlačítko **Přidat**.
56. V poli **Kniha** zadejte nebo vyberte hodnotu.
57. V poli **Zaúčtovat hodnotu** vyberte Zůstatková účetní hodnota.
58. Zadejte požadované hodnoty do pole **Hlavní účet**.
59. Zadejte požadované hodnoty do pole **Protiúčet**.
60. V poli **Odprodej nebo likvidace** vyberte „Likvidace“
61. Klikněte na tlačítko **Přidat**.
62. V poli **Kniha** zadejte nebo vyberte hodnotu.
63. V poli **Zaúčtovat hodnotu** vyberte Pořizovací hodnota.
64. Zadejte požadované hodnoty do pole **Hlavní účet**.
65. Zadejte požadované hodnoty do pole **Protiúčet**.
66. Klikněte na tlačítko **Přidat**.
67. V poli **Kniha** zadejte nebo vyberte hodnotu.
67. V poli **Zaúčtovat hodnotu** vyberte hodnotu Odpis (předchozí roky).  
68. Zadejte požadované hodnoty do pole **Hlavní účet**.
69. Zadejte požadované hodnoty do pole **Protiúčet**.
70. Klikněte na tlačítko **Přidat**.
71. V poli **Kniha** zadejte nebo vyberte hodnotu.
72. V poli **Zaúčtovat hodnotu** vyberte hodnotu Odpis (tento rok).
73. Zadejte požadované hodnoty do pole **Hlavní účet**.
74. Zadejte požadované hodnoty do pole **Protiúčet**.
75. Klikněte na tlačítko **Přidat**.
76. V poli **Kniha** zadejte nebo vyberte hodnotu.
77. V poli **Zaúčtovat hodnotu** vyberte hodnotu Opravy odpisů (předchozí roky).
78. Zadejte požadované hodnoty do pole **Hlavní účet**.
79. Zadejte požadované hodnoty do pole **Protiúčet**.
80. Klikněte na tlačítko **Přidat**.
81. V poli **Kniha** zadejte nebo vyberte hodnotu.
82. V poli **Zaúčtovat hodnotu** vyberte hodnotu Opravy odpisů (tento rok).
83. Zadejte požadované hodnoty do pole **Hlavní účet**.
84. Zadejte požadované hodnoty do pole **Protiúčet**.
85. Klikněte na tlačítko **Přidat**.
86. V poli **Kniha** zadejte nebo vyberte hodnotu.
87. V poli **Zaúčtovat hodnotu** vyberte Zůstatková účetní hodnota.
88. Zadejte požadované hodnoty do pole **Hlavní účet**.
89. Zadejte požadované hodnoty do pole **Protiúčet**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
