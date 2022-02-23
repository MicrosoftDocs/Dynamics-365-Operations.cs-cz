---
title: Návrh dotazníků
description: Tento článek popisuje postup vytváření dotazníku. Prvním krokem je návrh dotazníku. Při navrhování dotazníku můžete pouze zapsat otázky a odpovědi, ale také vytvořit strukturu, která umožňuje záznam a uspořádání odpovědí.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: da4250b281438c29c82150af8db9cb8cca41c6c9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417695"
---
# <a name="design-questionnaires"></a>Návrh dotazníků

Tento článek popisuje postup vytváření dotazníku. Prvním krokem je návrh dotazníku. Při navrhování dotazníku můžete pouze zapsat otázky a odpovědi, ale také vytvořit strukturu, která umožňuje záznam a uspořádání odpovědí. 

Pečlivě navržený dotazník pomáhá zvyšovat kvalitu dat, která shromažďujete. Díky promyšlenému návrhu můžete lépe a ve vhodný okamžik vybrat požadované otázky k dotazníku. Následující body vám pomohou naplánovat efektivní dotazník:

-   Jasně definovaný účel dotazníku je zajistit, aby otázky podporovaly účel.
-   Stanovte jednotlivce nebo skupiny osob, po kterých budete chtít dotazník vyplňovat.
-   Zadejte otázky, které se zobrazí v dotazníku, a zahrňte možnosti odpovědí, je-li třeba.
-   Ujistěte se, že dotazník logicky plyne, aby respondenti zůstali aktivní.
-   Otázky a odpovědi uspořádejte v pořadí, ve kterém se mají zobrazovat respondentům.
-   Rozhodněte se, jak by měly být vyhodnocovány výsledky, je-li třeba.
-   Rozhodněte, zda budete potřebovat další funkce. Například určete, zda a jak mají být výsledky kategorizovány, zda se požaduje časový limit nebo zda budou všechny otázky povinné.

Návrhová fáze zahrnuje čtyři kategorie úkolů, které je třeba dokončit v následujícím pořadí:

1.  Nastavte předpoklady podle potřeby.
2.  Nastavte skupiny odpovědí a odpovědi podle potřeby.
3.  Nastavte otázky a jejich přiřazení ke skupinám odpovědí.
4.  Nastavte dotazník jako takový a přiřaďte k němu otázky.

## <a name="prerequisites"></a>Požadavky
Některé předpoklady musí být stanoveny před vytvořením dotazníků, odpovědí a otázek. Avšak ne všechny předpoklady jsou nutné pro plnou funkčnost.

### <a name="required"></a>Požadováno

| Předpoklad        | Popis                |
|---------------------|----------------------------|
| Typy dotazníku | Kategorizujte dotazníky. |
| Typy otázek      | Kategorizujte otázky.      |

### <a name="optional"></a>Volitelné

| Předpoklad             | Popis                                                    |
|--------------------------|----------------------------------------------------------------|
| Parametry dotazníků | Upravte základní ovládací prvky a výchozí nastavení pro dotazníky. |

### <a name="questionnaire-types"></a>Typy dotazníku

Typy dotazníků jsou povinné a musí být přiřazeny při vytváření dotazníku. Typy dotazníku umožňují snadněji spravovat a klasifikovat dotazníky. Typy dotazníků slouží ke klasifikaci dotazníků a jejich odlišení od sebe navzájem. Pokud máte například několik dotazníků, ze kterých můžete vybírat, můžete je filtrovat podle typu a usnadnit tak hledání specifického dotazníku. Následuje několik příkladů typů dotazníku:

-   Rozvoj lidských zdrojů
-   Průzkumy odběratelů
-   Proces kontroly

### <a name="question-types"></a>Typy otázek

Typy otázek jsou povinné a musí být přiřazeny při vytváření otázky. 

Typy otázek se používají k rozdělení otázek do kategorií pro účely vykazování. Typy otázek také usnadňují hledání otázek, protože typy slouží jako filtry na stránce **Otázky**. Následuje několik příkladů typů otázek:

-   Lidské zdroje
-   Řízení podniku
-   Hodnocení kurzu

### <a name="questionnaire-parameters"></a>Parametry dotazníků

Parametry dotazníku jsou volitelné. Nemusíte je použít, v závislosti na požadavcích vaší společnosti. 

Parametry dotazníku definují anonymitu, kódy číselných řad a typy odkazů dotazníku. Když organizace distribuuje dotazník, může být třeba možnost respondentům umožnit, aby zůstali anonymní. 

Kódy číselných řad se používají k uspořádání otázek a odpovědí. Na základě těchto kódů číselných řad jsou hodnoty automaticky přiřazeny k položkám. 

Dříve než začnete definovat vaše data, měli byste definovat veškeré parametry. Vaše parametrů dotazníku můžete kdykoliv upravit.

## <a name="questionnaire-components"></a>Komponenty dotazníku
Dotazníky zahrnují tři hlavní prvky: skupiny odpovědí, které obsahují odpovědi pro otázky s možností více odpovědí, otázky a dotazník jako takový. Volitelně lze otázky v dotazníku seskupit do skupin výsledků. Skupiny výsledků umožňují rozdělit otázky do kategorií a poskytují další analýzy v dotazníku. 

[![Komponenty dotazníku](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### <a name="answer-groups-and-answers"></a>Skupiny odpovědí a odpovědi

Respondenti mohou na otázku odpovědět dvěma způsoby v závislosti na předmětu otázky:

-   Otevřené otázky nevyžadují odpovědi v určitém formátu. Respondenti mohou odpověď zadat jako text, číslo, datum nebo čas. Tyto otázky obvykle vyžadují, aby respondenti zadali subjektivní informace, jako je například názor, popis, hodnocení nebo odhad.
-   Uzavřené otázky vyžadují, aby respondent vybral odpověď ze seznamu možných správných odpovědí.

Chcete-li poskytnout seznam možných odpovědí pro uzavřené otázky, můžete vytvořit odpovědi na stránce **Skupiny odpovědí**. 

Skupiny odpovědí a odpovědi jsou součásti hlavní části informací, ze kterých jsou otázky vytvořeny. Po vytvoření skupiny odpovědí můžete skupinu odpovědí přiřadit k otázce v poli **Skupina odpovědí** na stránce **Otázky**. 

Skupinu odpovědí lze použít pro více otázek ve jednom dotazníku a pro více dotazníků. 

> [!NOTE]
> Pokud změníte textu odpovědi ve skupinách odpovědí, které již byly použity u vyplněných dotazníků, data může být obtížné vyhodnotit a výsledky dotazníku mohou být neplatné. Pokud musíte změnit skupinu odpovědí, zvažte vytvoření nové skupiny odpovědí namísto změny již existující skupiny. Skupiny odpovědí, které byly přiřazeny k určité otázce či odpovědi, nebo které byly zodpovězeny, není možné odstranit.

### <a name="questions"></a>Otázky

Dotazník musí obsahovat otázky. Otázky mohou být otevřené nebo uzavřené.

-   Odpovědi na otevřené otázky nejsou řízeny a respondenti mohou své odpovědi zadat.
-   Uzavřené otázky vyžadují seznam předdefinovaných možností odpovědí a otázky mohou být strukturovány tak, aby mohl respondent vybrat více odpovědí. Otázky by měly být formulovány tak, aby bylo možné od respondenta získat konkrétní informace a musí být propojeny se skupinou odpovědí, která obsahuje možnosti odpovědí pro každou uzavřenou otázku. 

    > [!NOTE]
    > Před nastavením uzavřených otázek je nutné vytvořit skupiny odpovědí a odpovědi.

Otázky lze uspořádat do hierarchie podmíněných otázek tak, aby druhotné otázky závisely na odpovědi, kterou respondent vybere pro předchozí otázku. Můžete nejprve napsat otázky a poté je uspořádat do hierarchie.

## <a name="setting-up-questionnaires"></a>Nastavení dotazníků

> [!NOTE]
> Před nastavením dotazníku je nutné nastavit odpovědi, dotazy a požadavky. 

U jednotlivých dotazníků lze určit následující údaje:

-   Celkový čas nebo časový limit pro zodpovězení povinných otázek.
-   Zda jsou všechny otázky povinné.
-   Zda mají být vypočítány body v dotazníku.
-   Jak mají být výsledky rozděleny do kategorií.
-   Zda bude dotazník k dispozici pro omezenou skupinu respondentů.
-   Zda má být šablona formuláře zobrazena jako pozadí každé stránky dotazníku.
-   Zda jsou nutné doplňující poznámky objasňující respondentům účel dotazníku.
-   Zda chcete zobrazit otázky v daném pořadí nebo je náhodně vybírat ze zdroje.
-   Zda budou otázky pokládány, pouze pokud byly pro předchozí odpovědi zadány konkrétní odpovědi.

### <a name="set-up-a-questionnaire"></a>Nastavení dotazníku

Primární stránka, kterou použijete k nastavení dotazníku, je stránka **Dotazníky**. Chcete-li nastavit dotazník, proveďte následující úkony v uvedeném pořadí:

1.  Vytvořte dotazník.
2.  Proveďte jeden z následujících kroků pro připojení otázek k dotazníku:
    -   Pokud používáte skupiny výsledků, otázky je možné přiřadit do dotazníku pomocí skupin výsledků. Nejprve nastavte skupiny výsledků dotazníku a pak přidejte do skupiny výsledků otázky.
    -   Pokud nepoužíváte skupiny výsledků, otázky je možné přiřadit přímo do dotazníku.

3.  Nastavte hierarchii podmíněných otázek, je-li třeba.
4.  Otestujte dotazník.

Na stránce **Dotazníky** kliknutím na možnost **Ověřit** otestujte, zda je dotazník správně sestaven. Doporučujeme však vyplnit otazník a otestovat jej sami před distribucí.

### <a name="modify-a-questionnaire"></a>Úprava dotazníku

Na stránce **Dotazníky** můžete provést následující úkoly:

-   Upravovat informace v dotazníku, například skupiny výsledků a otázky.
-   Odstraňovat a přidávat otázky.
-   Provádět změny ve skupinách výsledků a v pořadovém čísle. 

> [!CAUTION]
> Při provádění změn v dotaznících, které již byly zodpovězeny, postupujte opatrně. Změny mohou snížit přesnost statistiky, což může ovlivnit kvalitu podkladů pro vyhodnocení. Místo toho, abyste měnili otázku, která již byla zodpovězena, zvažte vytvoření nové otázky.

V dotazníku nelze odstranit následujících typy otázek:

-   Otázky, které jsou připojeny k dotazníku
-   Otázky, které již byly zodpovězeny a proto se zobrazí v dialogu **Odpovědi**.

### <a name="result-groups"></a>Skupiny výsledků

Při připojování otázek k dotazníku jsou skupiny výsledků volitelné. 

Skupiny výsledků se používají pro výpočet bodů a kategorizaci výsledků dotazníku. Při použití skupin výsledků můžete provádět následující úkoly:

-   Vyhodnoťte výsledky dotazníků na základě statistik bodů.
-   Vyhodnoťte výsledek respondenta pro každou skupinu výsledků, kterou nastavíte.
-   Generovat statistiku pro každou skupinu výsledků, což vám může pomoci analyzovat výsledky.
-   Vytiskněte sestavu, který zobrazuje výsledky pro každou skupinu výsledků a také volitelné body a texty, které jsou založeny na bodech získaných v každé skupině výsledků.

> [!NOTE]
> Před nastavením skupin výsledků je nutné dokončit následující úkoly:

-   Nastavte uzavřené otázky. Pro uzavřenou otázku musí být tato zadání na stránce **Otázky** nastavena na **Zaškrtávací políčko**, **Alternativní tlačítko** nebo **Pole se seznamem**.
-   Definujte body pro odpovědi ve skupinách odpovědí, které jsou přiřazeny jednotlivým otázkám.
-   Nastavte dotazník.

Chcete-li připojení otázky k dotazníku pomocí skupin výsledků, nejprve nastavte skupiny výsledků pro dotazník a pak přidejte do skupiny výsledků otázky. Pokud nepoužíváte skupiny výsledků, otázky je možné přiřadit přímo do dotazníku. 

Nastavte více skupin výsledků a vyhodnoťte body, které respondent získá za jednotlivé kategorie. Po vyplnění dotazníku můžete zobrazit body, které byly získány pro jednotlivé skupiny výsledků. 

> [!TIP]
> Chcete-li vyhodnocovat dotazník pomocí bodů, ale nikoli samostatných kategorií, můžete přidat všechny otázky do jedné skupiny výsledků. 

Pro každou skupinu výsledků můžete také nastavit jednu nebo více zpráv založených na bodech, které respondent získá po vyplnění dotazníku. Zobrazený text se může lišit v závislosti na výsledku, jehož respondenti dosáhnou ve skupině výsledků. Chcete-li použít zprávy založené na bodech, musíte definovat intervaly bodů a popis každého intervalu. Když respondent získá hodnocení určitého intervalu, bude text zahrnut do sestavy výsledků. 

Vzhledem k tomu, že skupina výsledků souvisí s body, které jsou přiřazeny konkrétní sadě otázek v dotazníku, můžete pro dotazník použít pouze určitou skupinu výsledků.

#### <a name="example-pointstexts-for-result-group-3"></a>Příklad: Body/text pro skupinu výsledků 3

Používáte dotazník pro test vedení s 15 otázkami ve třech kategoriích. Můžete vytvořit tři skupiny výsledků a přidat pět otázek pro každou skupinu výsledků. Body jsou poté sečteny ve třech skupinách. Tři skupiny výsledků jsou následující:

-   kreativní schopnosti,
-   vedoucí schopnosti,
-   technické schopnosti.

Chcete-li použít zprávy založené na bodech, nastavte intervaly textu pro každou skupinu výsledků. Každé otázce jsou přiděleny dva body. Maximální počet bodů v jednotlivých skupinách výsledků je tedy 10. 

Následující tabulka uvádí zprávy podle bodů, které definujete pro skupinu výsledků „schopnosti vedení“.

| Bodový interval | Text                                       |
|----------------|--------------------------------------------|
| 1 až 3         | Máte průměrné vůdcovské schopnosti.     |
| 4 až 7         | Máte dobré vůdcovské schopnosti.        |
| 8 až 10        | Máte výjimečné vůdcovské schopnosti. |

Můžete nastavit bodové intervaly a texty pro každou skupinu výsledků v dotazníku. Texty, které odpovídají hodnocení každého respondenta, jsou zobrazeny pro každou skupinu výsledků. 

> [!NOTE]
> Intervaly a texty lze měnit. Pokud však již byl dotazník vyplněn, mohou změny způsobit nesrovnalosti mezi předchozími a novými sestavami výsledků.

### <a name="conditional-question-hierarchies"></a>Hierarchie podmíněných otázek

Hierarchie podmíněných otázek jsou volitelné při nastavování dotazníku. 

> [!NOTE]
> Před nastavením hierarchie podmíněných otázek je třeba připojit otázky, které mají přiřazeny skupiny odpovědí k dotazníku. 

Chcete-li použít podmíněné otázky a vytvářet hierarchii otázek v dotazníku, můžete vytvořit posloupnost, ve které jsou otázky prezentovány, tak, aby závisela na odpovědi vybrané respondentem pro jednotlivé otázky. Pomocí úpravy posloupnosti otázek respondenta můžete dotazník upravit, kdy jej respondent vyplní.

#### <a name="examples"></a>Příklad

Právnická osoba nabízí zboží i služby zákazníkům. V takovém případě obvykle dochází k tomu, že někteří odběratelé kupují pouze zboží, jiní pouze služby a někteří zboží i služby. Proto pokud právnická osoba distribuuje průzkum spokojenosti zákazníků, použije na dotazník podmíněnou strukturu, aby odběratelé, kteří nakupují pouze služby, nemuseli odpovídat na otázky o zboží. 

Případně můžete nastavit dotazník tak, že pokud respondent vybere odpověď A na otázku 1, další v pořadí bude otázka 2. Pokud však respondent vybere odpověď B na otázku 1, následuje otázka 5.