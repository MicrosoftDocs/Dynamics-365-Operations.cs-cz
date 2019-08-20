---
title: Nastavení předpokladů pro správu neshody
description: Tento postup použijte pro povolení procesů správy neshod.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9094be37e44b978db224b16c255d04a36c5cefff
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845304"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Nastavení předpokladů pro správu neshody

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup použijte pro povolení procesů správy neshod. Neshoda popisuje postup nebo položku, která má potíže s kvalitou, a kde popisné informace zahrnují zdroj a typ problému. Tato procedura používá data ukázkové společnosti USMF. Tento postup obvykle provádí správce řízení kvality.


## <a name="enable-quality-management-processes-within-the-company"></a>Povolení procesů správy kvality v rámci společnosti
1. Přejděte do nabídky Řízení zásob > Nastavení > Parametry řízení zásob a skladu.
2. Klepněte na kartu Správa kvality.
3. Vyberte možnost Ano v poli Použít správu kvality.
    * Vyberte tento parametr, pokud chcete povolit proces správy kvality u společnosti.  
4. V poli Hodinová sazba je třeba zadat číslo.
    * Do pole Hodinová sazba zadejte hodinovou pracovní sazbu v místní měně. Hodinová sazba se používá pro výpočet nákladů na operace, které souvisejí s odstraněním neshody. Hodinová sazba a vypočtené náklady poskytují referenční informace o neshodách a navzájem se neovlivňují s dalšími funkcemi.  
5. Klikněte na Nastavení sestavy.
    * Tato stránka umožňuje definovat typy poznámek k sestavě kvality, které budou použity pro různé typy sestav správy kvality.  
6. Zavřete stránku.
7. Zavřete stránku.

## <a name="enable-user-for-nonconformance-processing"></a>Povolení zpracování neshody
1. Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.
    * Aby bylo možné zpracovat schválení neshody, uživatel, který schválí nebo zamítne neshodu, musí mít hodnotu "Název" přiřazenou na stránce Uživatelé. Aby bylo možné použít poznámky k dokumentům, uživatel musí také mít aktivováno řízení dokumentů v možnostech uživatele.  
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Jméno pomocí hodnoty „Ricardo“.
    * Filtr umožňuje vyhledat uživatele, který bude schvalovat nebo zamítat záznamy neshody.  
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Aby bylo možné zpracovat schválení neshody, uživatel, který schválí nebo zamítne neshodu, musí mít hodnotu "Název" přiřazenou na stránce Uživatelé.  
4. Klikněte na Možnosti uživatelů.
5. Klepněte na kartu Předvolby.
6. Vyberte možnost Ano v poli Povolit manipulaci s dokumenty.
    * Aby bylo možné použít poznámky k dokumentům, uživatel musí také mít aktivováno řízení dokumentů v možnostech uživatele.  
7. Zavřete stránku.
8. Zavřete stránku.
9. Zavřete stránku.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Definice typů diagnostiky v rámci zpracování neshod
1. Přejděte na Řízení zásob > Nastavení > Správa kvality > Typy diagnostiky.
    * Pomocí stránky Typy diagnostiky definujte klasifikaci akcí diagnostiky. Oprava určuje, jaký typ diagnostické akce má být proveden pro schválenou neshodu, kdo ji má provést a jaké je požadované a plánované datum dokončení.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Diagnostika.
4. Zadejte nějakou hodnotu do pole Popis.
5. Zavřete stránku.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Definice nákladů kvality v rámci zpracování neshod
1. Přejděte na Řízení zásob > Nastavení > Správa kvality > Náklady kvality.
    * Na stránce Náklady kvality definujte klasifikaci nákladů, které se použily v rámci operací souvisejících s neshodami.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Kód nákladů.
4. Zadejte nějakou hodnotu do pole Popis.
5. Zavřete stránku.

## <a name="define-the-operations-for-nonconformance-processing"></a>Definice operací v rámci zpracování neshod
1. Přejděte na Řízení zásob > Nastavení > Správa kvality > Operace.
    * Na stránce Operace definujte klasifikaci práce, která může být provedena pro schválenou neshodu. Přiřadíte-li k neshodě související operaci, můžete definovat informace o přiřazeném materiálu, pracovní době a různých poplatcích vyžadovaných pro provedení této operace. Tyto informace tvoří základ výpočtu odhadovaných nákladů na provedení operace.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Operace.
4. Zadejte nějakou hodnotu do pole Popis.
5. Zavřete stránku.

## <a name="define-problem-types-for-nonconformance-processing"></a>Definice typů problému v rámci zpracování neshod
1. Přejděte na Řízení zásob > Nastavení > Správa kvality > Typy problémů.
    * Na stránce Typy problémů definujte klasifikaci problémů s kvalitou, k nimž dochází u různých typů neshod. Mezi typy neshody patří: interní, odběratel, dodavatel, požadavek na službu, výroba a vedlejší produkt. Jeden typ problému může být spojen s několika typy neshod.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Typ problému.
4. Zadejte nějakou hodnotu do pole Popis.
5. Klikněte na Typy neshody.
    * Použijte stránku Typy neshody k povolení typu problému, který se má použít v jednom nebo více typech neshod. Typ problému zahrnující kód závady se může například vztahovat na všechny typy neshod, zatímco typ problému zahrnující stížnost odběratele se může týkat pouze typů neshod "odběratel" a "požadavek na službu".  
6. Klikněte na položku Nová.
7. Označte v seznamu vybraný řádek.
8. Vyberte volbu v poli Typ neshody.
9. Zavřete stránku.
10. Zavřete stránku.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Definice karanténních zóny ke zpracování neshod
1. Přejděte na Řízení zásob > Nastavení > Správa kvality > Karanténní zóny.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Karanténní zóna.
4. Zadejte nějakou hodnotu do pole Popis.
5. Zavřete stránku.

