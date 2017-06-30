---
title: "Správa neshod"
description: "Tento článek popisuje základní nastavení, které je vyžadováno při použití neshod. Pokud chcete použít objednávky kvality, je třeba provést další nastavení."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4aebabfc6160393e5c817cd07af835d3b1268c2e
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="nonconformance-management"></a>Správa neshod

[!include[banner](../includes/banner.md)]


Tento článek popisuje základní nastavení, které je vyžadováno při použití neshod. Pokud chcete použít objednávky kvality, je třeba provést další nastavení. 

Pokud chcete zapnout správu neshody, postupujte takto:

1.  Definujte parametry zásob a správy skladu související s neshodami:
    -   Volbu **Použít správu kvality** nastavte na hodnotu **Ano**.
    -   Do pole **Hodinová sazba** zadejte hodinovou pracovní sazbu v místní měně. Hodinová sazba se používá pro výpočet nákladů na operace, které souvisejí s neshodou. Hodinová sazba a vypočtené náklady poskytují referenční informace o neshodách. S ostatními funkcemi nespolupracují.
    -   K definování typu dokumentu pro tisk použijte kartu **Správa kvality** na stránce **Nastavení sestavy**. Můžete vytisknout sestavu neshod, značku neshody nebo sestavu oprav. Definovat lze více než jeden záznam pro tisk různých typů dokumentu nebo pro tisk intenrích a externích poznámek. Je užitečné použít stránku **Typ dokumentu** k definici jedinečného typu dokumentu pro neshody a jedinečného typu dokumentu pro opravy. Můžete například zadat poznámky o neshodě pomocí jedinečného typu dokumentu pro neshody. V takovém případě určete jedinečný typ dokumentu v možnostech sestavy.
    -   Povolte číselné řady pro neshody a opravu odkazů.

2.  Povolte schválení neshod uživatelem. Pomocí pole **Název** na stránce **Uživatelé** přiřaďte ke každému uživateli zaměstnance, který musí neshodu schválit. Systém použije zaměstnance, kteří mění stav neshody, ke sledování historie neshody. Uživatelé nemohou neshodu schválit, pokud jim nebyl přidělen identifikátor zaměstnance.
3.  Definujte typy problémů, které se k neshodám přiřadí. Na stránce **Typy problémů** definujte klasifikaci problémů s kvalitou, k nimž dochází u různých typů neshod. Můžete nastavit následující typy neshod: **Interní**, **Odběratel**, **Dodavatel**, **Požadavek na službu**, **Výroba** a **Výroba vedlejších produktů**. Použijte stránku **Typy neshody** k povolení typu problému, který se má použít v jednom nebo více typech neshod. Typ problému zahrnující kód závady může například souviset se všemi typy neshod, zatímco typ problému zahrnující stížnost odběratele se může týkat pouze typů neshod **Odběratel** a **Požadavek na službu**.
4.  Definujte karanténní zóny poskytující rámcové vedení při manipulaci s vadným materiálem. K definici zón, které lze neshodě přiřadit, použijte stránku **Karanténní zóny**. Na tištěné značce neshody se zobrazí přiřazená karanténní zóna a informace o použití, které poskytují návod při manipulaci s vadným materiálem. Zóny mohou odpovídat umístěním zásob nebo provozním prostředkům.
5.  Definujte typy diagnostiky, které budou přiřazeny k opravám. Pomocí stránky **Typy diagnostiky** definujte klasifikaci akcí diagnostiky. Oprava určuje, jaký typ diagnostické akce se má provést pro schválenou neshodu a kdo ji má provést. Určuje rovněž požadované datum dokončení a plánované datum dokončení.
6.  Definujte související operace, které budou k neshodám přiřazeny. Na stránce **Operace** definujte klasifikaci práce, která může být provedena pro schválenou neshodu. Přiřadíte-li k neshodě související operaci, můžete poskytnout podrobné informace, například o přiřazeném materiálu, pracovní době a různých poplatcích vyžadovaných pro provedení této operace. Tyto informace se používají k výpočtu odhadovaných nákladů na danou operaci. Podrobné informace a odhad nákladů jsou pouze informativní. Související operace pro kvalitu se liší od operací, které lze definovat ve výrobním postupu.


<a name="see-also"></a>Viz také
--------

[Vytvoření a zpracování neshody (průvodce záznamem úloh)](https://ax.help.dynamics.com/en/wiki/create-and-process-a-nonconformance/)

[Procesy správy kvality](quality-management-processes.md)

[Nastavení předpokladů pro správu neshody (průvodce záznamem úloh)](https://ax.help.dynamics.com/en/wiki/set-up-prequisites-for-nonconformance-management/)




