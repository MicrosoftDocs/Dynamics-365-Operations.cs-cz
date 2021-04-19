---
title: Nastavení předpokladů pro správu neshody
description: Toto téma použijte pro povolení procesů správy neshod.
author: perlynne
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8ce4ae69585a93d679ae614ae81efc9723d9397
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818174"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Nastavení předpokladů pro správu neshody

[!include [banner](../../includes/banner.md)]

Toto téma použijte pro povolení procesů správy neshod. Neshoda popisuje postup nebo položku, která má potíže s kvalitou, a kde popisné informace zahrnují zdroj a typ problému. Tato procedura používá data ukázkové společnosti USMF. Tento postup obvykle provádí správce řízení kvality.


## <a name="enable-quality-management-processes-within-the-company"></a>Povolení procesů správy kvality v rámci společnosti
1. V navigačním podokně přejděte na **Moduly > Řízení zásob > Nastavení > Parametry řízení zásob a skladu**.
2. Vyberte kartu **Správa kvality**.
3. Vyberte **Ano** v poli **Použít správu kvality**, chcete-li povolit procesy správy kvality pro společnost.
4. Do pole **Hodinová sazba** zadejte částku v místní měně. Hodinová sazba se používá pro výpočet nákladů na operace, které souvisejí s odstraněním neshody. Hodinová sazba a vypočtené náklady poskytují referenční informace o neshodách a navzájem se neovlivňují s dalšími funkcemi.  
5. Vyberte **Nastavení sestavy**, chcete-li definovat typy poznámek k sestavě kvality, které budou použity pro různé typy sestav správy kvality.

## <a name="enable-user-for-nonconformance-processing"></a>Povolení zpracování neshody
1. V navigačním podokně přejděte na **Moduly > Správa systému > Uživatelé > Uživatelé**. 
2. Rychlý filtr umožňuje vyhledat uživatele, který bude schvalovat nebo zamítat záznamy neshody. Můžete například filtrovat v poli **Jméno** pomocí hodnoty `Ricardo`. Aby bylo možné zpracovat schválení neshody, uživatel, který schválí nebo zamítne neshodu, musí mít hodnotu „Název“ přiřazenou na stránce **Uživatelé**. Aby bylo možné použít poznámky k dokumentům, uživatel musí také mít aktivováno řízení dokumentů v možnostech uživatele.  
3. Označte řádek požadovaného záznamu.
4. Vyberte **Možnosti uživatele**.
5. Vyberte kartu **Předvolby**.
6. Vyberte možnost **Ano** v poli **Povolit manipulaci s dokumenty**.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Definice typů diagnostiky v rámci zpracování neshod
1. V podokně navigace přejděte na **Moduly > Řízení zásob > Nastavení > Správa kvality > Typy diagnostiky**. Pomocí stránky **Typy diagnostiky** definujte klasifikaci akcí diagnostiky. Oprava určuje, jaký typ diagnostické akce má být proveden pro schválenou neshodu, kdo ji má provést a jaké je požadované a plánované datum dokončení.  
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Diagnostika**.
4. Zadejte hodnotu do pole **Popis**.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Definice nákladů kvality v rámci zpracování neshod
1. V podokně navigace přejděte na **Moduly > Řízení zásob > Nastavení > Správa kvality > Náklady kvality**. Na stránce **Náklady kvality** definujte klasifikaci nákladů, které se použily v rámci operací souvisejících s neshodami.  
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Kód nákladů**.
4. Zadejte hodnotu do pole **Popis**.

## <a name="define-the-operations-for-nonconformance-processing"></a>Definice operací v rámci zpracování neshod
1. V podokně navigace přejděte na **Moduly > Řízení zásob > Nastavení > Správa kvality > Operace**. Na stránce **Operace** definujte klasifikaci práce, která může být provedena pro schválenou neshodu. Přiřadíte-li k neshodě související operaci, můžete definovat informace o přiřazeném materiálu, pracovní době a různých poplatcích vyžadovaných pro provedení této operace. Tyto informace tvoří základ výpočtu odhadovaných nákladů na provedení operace.  
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Operace**.
4. Zadejte hodnotu do pole **Popis**.

## <a name="define-problem-types-for-nonconformance-processing"></a>Definice typů problému v rámci zpracování neshod
1. V podokně navigace přejděte na **Moduly > Řízení zásob > Nastavení > Správa kvality > Typy problémů**. Na stránce **Typy problémů** definujte klasifikaci problémů s kvalitou, k nimž dochází u různých typů neshod. Mezi typy neshody patří **Interní**, **Odběratel**, **Dodavatel**, **Požadavek na službu**, **Výroba** a **Vedlejší produkt**. Jeden typ problému může být spojen s několika typy neshod.  
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Typ problému**.
4. Zadejte hodnotu do pole **Popis**.
5. Vyberte **Typy neshody**. Použijte stránku **Typy neshody** k povolení typu problému, který se má použít v jednom nebo více typech neshod. Typ problému zahrnující kód závady se může například vztahovat na všechny typy neshod, zatímco typ problému zahrnující stížnost odběratele se může týkat pouze typů neshod "odběratel" a "požadavek na službu".  
6. Zvolte **Nové**.
7. Vyberte volbu v poli **Typ neshody** na novém řádku.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Definice karanténních zóny ke zpracování neshod
1. V podokně navigace přejděte na **Moduly > Řízení zásob > Nastavení > Správa kvality > Karanténní zóny**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Karanténní zóna**.
4. Zadejte hodnotu do pole **Popis**.
5. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]