---
title: Finanční odsouhlasení v maloobchodních prodejnách
description: Toto téma popisuje finanční odsouhlasení v maloobchodních prodejnách pro POS pro aplikaci Microsoft Dynamics 365 Commerce.
author: anpurush
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2afe967248136e9b658e1ee18053a54ab3f0d325c088a5eb2e522fac335c01f0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752452"
---
# <a name="financial-reconciliation-in-retail-stores"></a>Finanční odsouhlasení v maloobchodních prodejnách

[!include [banner](includes/banner.md)]

V aplikaci Microsoft Dynamics 365 Commerce verze 10.0.10 nebo starší umožňuje funkce, kterou disponuje klientská aplikace pokladního místa (POS) pro účely denních uzavíracích operací v maloobchodních prodejnách, pracovníkům a manažerům prodejen provádět denní uzavírací operace. Mohou například zpracovávat výkazy úhrad, uzavírat směny bez zadání částky, odsouhlasovat transakce v rámci směn nebo uzavírat směny. V POS však neexistuje žádná funkce umožňující uzavřít finanční údaje za směnu, kterou by bylo možné použít k odeslání finančních údajů do systému Commerce Headquarters. Za provedení této úlohy obvykle nesou odpovědnost manažeři obchodu. Než mohou uzavřít směnu, musí zkontrolovat informace, provést potřebné opravy a finalizovat souhrnné údaje za směnu. Konečné součty by pak měly být zaúčtovány do finančních modulů v systému Commerce Headquarters.

Kromě toho systém Commerce ve verzi 10.0.10 nebo starší umožňuje manažerům obchodu kontrolovat a upravovat řádky výpisů v systému Commerce Headquarters. Tato funkčnost je však omezená a manažeři obchodu mají málokdy možnost přístup ke klientu Commerce Headquarters. Kontrolu a úpravu maloobchodního finančního výkazu lze navíc provést pouze tehdy, když jsou výkazy vytvořeny v systému Commerce Headquarters. Tento proces se však obvykle spouští přes noc. Manažeři obchodu proto musí počkat s uzavřením směny do vytvoření finančních maloobchodních výkazů v systému Commerce Headquarters.

V systému Commerce verze 10.0.11 nebo novější mohou manažeři obchodů kontrolovat, upravovat a finalizovat změny přímo v klientu POS. Příslušná data se pak použijí k vytvoření a zaúčtování maloobchodních finančních výkazů v systému Commerce Headquarters.

> [!NOTE]
> Funkce, jež souvisí s finančním odsouhlasením v maloobchodních prodejnách, funguje pouze v případě, že je zapnuta postupná tvorba objednávek. Další informace uvádí téma [Postupné vytváření objednávek pro maloobchodní transakce](trickle-feed.md).

## <a name="set-up-financial-reconciliation"></a>Nastavení finančního odsouhlasení

Chcete-li používat funkci finančního odsouhlasení, postupujte takto.

1. V pracovním prostoru **Správa funkcí** zapněte funkci **Výkazy maloobchodu – Postupné**.
1. V profilu funkcí POS příslušného obchodu nastavte u možnosti **Povolit finanční odsouhlasení v obchodě** hodnotu **Ano**.

## <a name="more-information-about-financial-reconciliation"></a>Další informace o finančním odsouhlasení

Když je funkce finančního odsouhlasení zapnuta, některé parametry definované na záložce s náhledem **Výkaz/uzávěrka** na stránce **Maloobchodní prodejny** v systému Commerce Headquarters jsou synchronizovány s databází kanálů. Uplatňuje se stejná sada výpočtových kritérií a mezních hodnot, jaké se používají pro výkazy maloobchodu.

Když je vyvolána operace **Uzavření směny**, systém ověří, že se částky vypočítané systémem a deklarované částky shodují. Pokud se liší a rozdíl překročí definované mezní hodnoty, je uživatel vyzván, aby provedl potřebné úpravy.

U každé úhrady lze provést úpravy. Když je vybrána úhrada, může uživatel zobrazit součty pro různé typy transakcí a součty pro konkrétní typ transakce upravovat. Během úpravy systém zobrazuje původní vypočítanou částku a přepsanou částku pro daný typ transakce. Uživatel může také v rámci procesu úprav zaznamenávat poznámky. Poznámky lze použít pro auditní účely.

Uživatelé mohou ignorovat výzvy a zprávy týkající se ověření a mohou pokračovat v procesu uzavírání směny. Pokud však uživatel výzvy k ověření ignoruje, nastanou stejné problémy a bude nutné je opravit, až se finanční výkazy směny zaúčtují v systému Commerce Headquarters.

Operace **Uzavření směny** v POS také ověřuje, že jsou všechny transakce v offline databázi synchronizovány s databází kanálů. Pokud nějaké transakce synchronizovány nejsou, uživatel obdrží varovnou zprávu, protože taková situace by mohla způsobit nesprávný výpočet systémových částek. V této situaci může uživatel operaci **Uzavření směny** ukončit a pokusit se synchronizovat offline transakce s databází kanálů. Další možností je, že uživatel může ručně upravit částky vypočítané systémem tak, aby zohledňovaly nesynchronizované transakce, aby byla finalizována a zaúčtována správná sada finančních údajů. 

Pokud se používá postupné účtování, jež zajišťuje oddělení účtování transakcí od finančního účtování, můžete rozhodnout, že pro chybějící offline transakce je možné částky vypočítané systémem upravit. Tímto způsobem zajistíte, že finanční údaje budou vždy účtovány a zaúčtovány správně, bez ohledu na chybějící transakce. Offline transakce lze synchronizovat s databází kanálů a systémem Commerce Headquarters a zaúčtovat je později, odděleně od finančního účtování.

Podrobnosti o finančním odsouhlasení za směnu jsou synchronizovány se systémem Commerce Headquarters pomocí úlohy P-job.

Výkazy finančního maloobchodu v systému Commerce Headquarters nepočítají součty, jež se zobrazují v podrobnostech na řádcích výkazů. Místo toho se k tvorbě a zaúčtování maloobchodních výkazů používají finalizované částky v klientu POS.


[!INCLUDE[footer-include](../includes/footer-banner.md)]