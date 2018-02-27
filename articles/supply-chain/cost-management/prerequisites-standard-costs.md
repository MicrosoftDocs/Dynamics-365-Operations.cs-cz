---
title: "Předpoklady pro standardní náklady"
description: "V tomto tématu je popsán základní postup při použití standardních nákladů."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e63f2b4289b640e601492425331ea8f3804d139a
ms.openlocfilehash: 4f505a2de89863d1a12d415795fdfb82b3557bc0
ms.contentlocale: cs-cz
ms.lasthandoff: 01/17/2018

---

# <a name="prerequisites-for-standard-costs"></a>Předpoklady pro standardní náklady

[!include[banner](../includes/banner.md)]


V tomto tématu je popsán základní postup při použití standardních nákladů. Následné kroky závisí na operacích dané společnosti. Kroky se například liší pro nevýrobní prostředí, výrobní prostředí bez postupů nebo výrobní prostředí s postupy. 

Chcete-li nastavit standardní náklady, postupujte následujícím způsobem.

**1. Vytvořte skupinu modelů položek pro standardní náklady.**

Použijte stránku **Skupiny modelů položek** pro vytvoření nové skupiny pro standardní náklady a přiřaďte model zásob **standardních nákladů**. Identifikátor pro skupinu modelů položek by měl být popisný, jako například **Std Nákl**. Zaškrtnutím příslušných políček určete, že pro danou skupinu má být povoleno použití záporného finančního skladu a zaúčtovány fyzické zásoby a finanční zásoby. Tato skupina standardních nákladů bude přiřazena položkám.

**2. Definujte účty hlavní knihy, které odpovídají odchylkám standardních nákladů.** 

Prostřednictvím stránky **Účtová osnova** definujte účty hlavní knihy, které odpovídají odchylkám standardních nákladů. Tyto účty hlavní knihy musí být definovány před přiřazením na stránce **Zaúčtování**. Účty hlavní knihy mohou odrážet skupiny položek a skupiny nákladů.

**3. Přiřaďte účty hlavní knihy k zaúčtováním položek, které odpovídají odchylkám standardních nákladů.** 

Pomocí stránky **Zaúčtování** proveďte přiřazení účtů hlavní knihy, které odpovídají odchylkám standardních nákladů. Můžete určit, zda mají být účty hlavní knihy pro odchylky specifikovány podle položky (nebo skupiny položek) a podle nákladové skupiny (nebo typu nákladové skupiny), nebo můžete zadat, že účet hlavní knihy se vztahuje ke všem položkám a všem nákladovým skupinám. Tyto volby odpovídají nákladovým vztahům pro tabulky, skupiny a všechny položky. 

Před definováním pravidel zaúčtování položky povolte prostřednictvím stránky **Kombinace transakcí** použití nákladových vztahů (pro tabulky, skupiny a všechny položky).

**4. Definujte parametry zásob, které odpovídají standardním nákladům.** 

-  Použijte kartu **Kusovníky** na stránce **Parametry zásob** s cílem definovat dva parametry řízení nákladů, které odpovídají standardním nákladům. 

    -  V poli **Rozúčtování nákladů** vyberte možnost **Žádné** nebo **Dílčí hlavní kniha**. Vyberete-li **Dílčí hlavní kniha**, rozúčtování nákladů je *aktivní* rozúčtování nákladů. Aktivní rozúčtování nákladů je velmi důležité pro výpočet, zachování a zobrazení rozdělení nákladových skupin do segmentů napříč víceúrovňovou strukturou produktů pro standardní nákladové položky. Je-li rozúčtování nákladů aktivní, můžete vykázat a analyzovat zásoby, nedokončenou výrobu (NV) a náklady na prodané zboží (COGS) pro jednotlivé nákladové skupiny ve formátu s jednou úrovní, s více úrovněmi nebo v souhrnném formátu. Když je rozúčtování nákladů aktivní a aktivujete náklady na vyráběnou položku, segmentace nákladových skupin se uloží v záznamu nákladů položky. 

    -  Vyberete-li **Žádné**, segmentace nákladových skupin nebude pro standardní nákladové položky zachována. Jinak řečeno, standardní náklady na vyráběnou položku budou vypočteny a spravovány jako jedna částka bez rozdělení nákladových skupin do segmentů. Nákladové příspěvky vyráběných součástí budou agregovány do jediné částky.

-  V poli **Odchylky od standardních hodnot** vyberte **Souhrn** nebo **Na nákladovou skupinu**. Volba **Na nákladovou skupinu** vám umožňuje identifikovat odchylky nákupní ceny a odchylky výroby podle nákladové skupiny. Můžete také identifikovat čtyři typy výrobních odchylek: velikost šarže, množství, cena a odchylky náhrady. Volba **Souhrn** znamená, že nelze identifikovat odchylky podle nákladové skupiny a že nelze identifikovat čtyři typy výrobních odchylek. Můžete zobrazit pouze souhrnnou výrobní odchylku.

-  Zásady týkající se odchylek vzhledem ke standardním hodnotám pracují nezávisle na zásadách rozúčtování nákladů. To znamená, že můžete vybrat zásadu pro rozúčtování nákladů **Žádná** a přitom vybrat odchylky podle nákladových skupin, takže budou stále zaznamenány výrobní odchylky podle nákladových skupin.

**5. Vytvořte nákladové verze pro standardní náklady.** 

Prostřednictvím stránky **Nastavení nákladové verze** vytvořte jednu nebo více nákladových verzí pro standardní náklady. Každá nákladová verze musí být označena s použitím nákladového typu pro **Standardní náklady** a umožňovat, aby obsah zahrnoval data nákladů.

**6. Připravte existujícího odběratele v aplikaci na použití standardních nákladů.** 

Odběratelé, kteří chtějí změnit existující položky na skladový model standardních nákladů, musí použít stránku **Převody standardních nákladů**.


<a name="related-topics"></a>Související témata
--------

[Přehled převodu standardních nákladů](standard-cost-conversion-overview.md)

