---
title: Předpoklady pro převod standardních nákladů
description: Toto téma popisuje úkoly prováděné před spuštěním převodu standardních nákladů.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da5605e3542cfb8803b6a9f3645bcb2cc613c0bd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423985"
---
# <a name="prerequisites-for-a-standard-cost-conversion"></a>Předpoklady pro převod standardních nákladů

[!include [banner](../includes/banner.md)]

Toto téma popisuje úkoly prováděné před spuštěním převodu standardních nákladů. 

Před spuštěním standardního převodu nákladů postupujte takto:

1.  Definujte **skupinu modelů zboží** pro standardní náklady. Na stránce Skupiny modelů položek vytvořte skupinu modelů zboží, která používá skladový model standardních nákladů. Při nastavení převodu standardních nákladů přiřaďte tuto skupinu modelů zboží převáděným položkám.
2.  Přiřaďte ke každé položce odpovídající **skupinu nákladů**.
    -   Nákladová skupina přiřazená k zakoupené položce může sloužit jako základ pro přiřazení účtů hlavní knihy, které souvisí se standardními náklady. Ty mohou zahrnovat přiřazení účtů hlavní knihy pro odchylky nákupní ceny. Ve výrobním prostředí poskytuje skupina nákladů, která je přiřazena k zakoupeným komponentám, také rozdělení nákladů ve vypočtených nákladech na vyráběné položky.
    -   Skupina nákladů přiřazená vyrobené položce může sloužit jako základ pro přiřazení účtů hlavní knihy, které souvisí se standardními náklady, jako je například přiřazení účtů hlavní knihy odchylkám výroby.

3.  Přiřaďte k vyráběné položce **standardní množství objednávky**, pokud má konstantní náklady. Standardní množství objednávky pro vyráběnou položku je používáno jako účetní velikost šarže pro amortizaci nebo určení průběžných či konstantních nákladů. Ty mohou zahrnovat časy nastavení v operacích postupu nebo konstantní množství komponent v kusovníku.
4.  Přiřaďte **účty hlavní knihy**, které souvisí se standardními náklady, především s odchylkami přecenění. Pomocí stránky **Zaúčtování** (**Řízení zásob** &gt; **Nastavení**) proveďte přiřazení účtů hlavní knihy, které souvisí se standardními náklady. Jako minimální hodnotu procesu převodu standardních nákladů je nutné přiřadit účet pro odchylku přecenění všech položek a všech nákladových skupin. Stránka **Účtová osnova** slouží k definování účtů hlavní knihy, které budou vyžadovány pro standardní náklady. Před definováním pravidel zaúčtování zboží povolte prostřednictvím stránky **Kombinace transakcí** použití nákladových vztahů (pro tabulky, skupiny a všechny položky).
5.  Definujte parametry zásob, které odpovídají standardním nákladům. Pomocí karty **Číselné řady** na stránce **Parametry řízení zásob a skladu** proveďte přiřazení číselné řady k dokladům přecenění. Doklad přecenění je generován v případě, že výsledkem převodu standardních nákladů je změna skladové hodnoty položky. Pomocí stránky **Parametry řízení zásob a skladu** definujte parametry řízení nákladů (na kartě **Skladové účetnictví**) a tím definujte dva parametry, které souvisí se standardními náklady.
    -   Pomocí pole **Rozúčtování nákladů** vyberte možnost Ne nebo Dílčí hlavní kniha. Volba Dílčí hlavní kniha odpovídá termínu aktivní rozúčtování nákladů. Aktivní rozúčtování nákladů je velmi důležité pro výpočet, zachování a zobrazení rozdělení nákladových skupin do segmentů napříč víceúrovňovou strukturou produktů pro standardní nákladové položky. Je-li rozúčtování nákladů aktivní, můžete vykázat a analyzovat následující údaje v jednoúrovňovém, víceúrovňovém nebo celkovém formátu:
        1.  Zásoby
        2.  Nedokončená výroba (NV)
        3.  Náklady prodaného zboží podle nákladových skupin

        Aktivní rozúčtování nákladů znamená, že povolení nákladů na vyráběnou položku bude mít za výsledek uložení segmentace nákladových skupin v záznamu nákladů položky. Pokud nevložíte žádnou hodnotu do pole **Rozúčtování nákladů**, nebude pro standardní nákladové položky udržována segmentace nákladových skupin. To tedy znamená, že standardní náklady na vyráběnou položku budou vypočteny a spravovány jako jedna částka bez rozdělení nákladových skupin do segmentů a že nákladové příspěvky vyráběných součástí budou agregovány do jediné částky.
    -   Pomocí pole **Odchylky od standardních hodnot** vyberte sumarizované údaje nebo údaje podle nákladových skupin. Volba podle nákladových skupin umožňuje identifikovat odchylky nákupní ceny a odchylky výroby podle nákladové skupiny. To také umožňuje identifikovat čtyři typy výrobních odchylek (velikost šarže, množství, cena a odchylky náhrady). Volba sumarizace znamená, že nelze identifikovat odchylky podle nákladové skupiny a že nelze identifikovat čtyři typy výrobních odchylek. Můžete zobrazit pouze souhrnnou výrobní odchylku. Zásady týkající se odchylek vzhledem ke standardním hodnotám pracují nezávisle na zásadách rozúčtování nákladů. To znamená, že nemusíte vybrat žádnou zásadu pro rozúčtování nákladů a přitom vybrat odchylky podle nákladových skupin, takže budou stále zaznamenány výrobní odchylky podle nákladových skupin.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]