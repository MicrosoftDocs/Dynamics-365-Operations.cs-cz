---
title: Kusovníky šablony
description: Kusovník šablony poskytuje standardní seznam součástí pro předměty servisu, o které pravidelně pečujete.
author: ShylaThompson
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab8586f81dc4a897d243b9d289109f039c390fcbf90c5c205125cf49eb5e8e39
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724741"
---
# <a name="template-boms"></a>Kusovníky šablony    

[!include [banner](../includes/banner.md)]


Kusovník šablony poskytuje standardní seznam součástí pro předměty servisu, o které pravidelně pečujete. Součásti uvedené v kusovníku šablony představují jednotlivé dílčí součásti předmětu servisu. Když na předmět servisu použijete kusovník šablony, můžete uchovávat záznam dílčích součástí, které byly v předmětu servisu vyměněny.

Použití kusovníku šablony na servisní smlouvu nebo zakázku vyžaduje jeho připojení ke vztahu předmětu servisu.


> [!NOTE]
> <P>Na předmět servisu lze použít pouze jeden kusovník šablony.</P>

## <a name="create-a-template-bom"></a>Vytvoření šablony kusovníku

Následující tabulka obsahuje informace o různých metodách používaných k vytvoření šablony Kusovníku.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Metoda</p></th>
<th><p>popis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Výrobní</p></td>
<td><p>Šablona kusovníku je založena na výrobní zakázce. Tato možnost je k dispozici pouze v případě, že pracujete v produkčním prostředí. Výhodou je, že máte aktuální, podrobný seznam součástí, které tvoří položku.</p></td>
</tr>
<tr class="even">
<td><p>Položka BOM</p></td>
<td><p>Šablona kusovníku je vytvořena na základě kusovníku položky. Kusovník položky, na rozdíl od výrobního Kusovníku, je statický seznam součástí, ze kterých je položka sestavena.</p></td>
</tr>
<tr class="odd">
<td><p>Stávající šablona</p></td>
<td><p>Tato šablona je vytvořena na základě existujícího kusovníku položky.</p></td>
</tr>
<tr class="even">
<td><p>Ruční</p></td>
<td><p>Pokud víte, které náhradní díly obvykle měníte v předmětu servisu, můžete ručně vytvořit šablonu kusovníku. Tato metoda napomáhá k zajištění, že součásti, které jsou zahrnuty do šablony, odpovídají skutečným požadavkům vašeho pracoviště.</p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>Použití kusovníku šablony na servisní smlouvu nebo zakázku

Kusovník šablony můžete použít na servisní smlouvu nebo servisní zakázku nebo na obojí. Servisní smlouva obvykle pokrývá dlouhodobou spolupráci s odběratelem. Užitečnými informacemi, které je třeba zaznamenat v servisní smlouvě, je historie výměn, která jsou sledovány v servisním kusovníku.

Šablonu Kusovníku lze také použít na servisní zakázku a zaznamenávat historii služby, která byla provedena v předmětu servisu.

## <a name="copy-the-history-of-a-service-bom"></a>Zkopírování historie servisního kusovníku

Historii řádků servisního kusovníku lze zkopírovat z jedné servisní smlouvy do jiné smlouvy. Zkopírováním historie servisu mezi smlouvami můžete zachovat záznam o výměnách položky.

**Příklad**

Uzavřeli jste tříletou servisní smlouvu na auto odběratele. Během tohoto období si odběratel zvykne na vysokou úroveň služeb, kterou společnost poskytuje. Proto po vypršení smlouvy chce tento zákazník zadat novou. Máte nyní možnost dohodnout výhodnější smluvní podmínky pro společnost. Vzhledem k tomu, že záznamy o vyměněných součástech mohou být v budoucnosti užitečné, zkopírujete historii servisního kusovníku do nové smlouvy.

## <a name="modify-the-template-bom"></a>Úprava kusovníku šablony

Pokud šablona Kusovníku nebyla připojena k předmětu servisu, můžete z ní upravit nebo odstranit řádky. Po připojení šablony Kusovníku k určitému předmětu servisu můžete upravit místní verzi Kusovníku. Pokud chcete duplikovat nastavení místní verze Kusovníku šablony, můžete vytvořit novou šablonu Kusovníku na základě místní verze. Další informace získáte v tématu [Změna kusovníku služby](modify-service-bom.md).

Pokud nahradíte položku v kusovníku, můžete výměnu zaznamenat v řádku kusovníku, který je k dispozici v návrháři kusovníku. Volitelně můžete pro vyměněný objekt vystavit fakturu. Jestliže vytvoříte řádek servisní zakázky, můžete pro vyměněnou součást vystavit fakturu. Pokud pro výměnu nevytvoříte řádek servisní zakázky, uchovají se pro vaše záznamy informace o výměně a sleduje se historie předmětu servisu.

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>Změna způsobu zobrazení informací na řádku Kusovníku

Pro všechny kusovníky šablon a servisní kusovníky můžete určit, jakým způsobem se mají zobrazovat informace z řádků kusovníků. Tyto změny se vztahují na všechny kusovníky šablony a kusovníky servisu. Patří sem ty, které jsou připojeny k předmětům servisu.

## <a name="set-up-number-sequences-for-template-boms"></a>Nastavení číselných řad pro kusovníky šablony

Chcete-li používat kusovníky šablony, je nutné nastavit dvě číselné řady. Jedna řada je určená pro kusovník šablony a druhá pro číslování řádků historie kusovníku.


> [!NOTE]
> <P>Číselné řady se používají k přidělování identifikátorů k záznamům, které je vyžadují. Aby bylo možné přiřadit číselnou řadu pro Kusovník šablony nebo číslo řádku historie Kusovníku, musíte nastavit kódy číselných řad.</P>


## <a name="set-up-number-sequences"></a>Nastavit číselné řady

1.  Na stránce se seznamem **číselné řady** vytvořte číselné řady pro kusovníky šablony a čísla řádků historie Kusovníku. 

2.  Klikněte **Správa servisu** \> **Nastavení** \> **Parametry správy servisu**.

3.  Klepněte na tlačítko **číselné řady** a vyberte kód číselné řady pro reference číselné řady, které jste vytvořili ve formuláři **číselné řady**.

4.  Uložte změny zavřením formuláře.


> [!NOTE]
> <P>Číslo řádku historie Kusovníku používá systém k přidružení transakcí v historii Kusovníku k servisní smlouvě nebo servisní zakázce. Číslo řádku historie kusovníku se nezobrazuje v uživatelském rozhraní.</P>



## <a name="see-also"></a>Viz také

[Vytvoření šablony kusovníku](create-template-bom.md)

[Správa šablon kusovníku pro vztahy předmětu](manage-template-boms-on-object-relations.md)

[Změna servisního kusovníku](modify-service-bom.md)

 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]