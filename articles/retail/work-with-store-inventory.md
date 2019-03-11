---
title: Správa skladových zásob
description: Toto téma popisuje typy dokumentů, které můžete použít ke správě zásob.
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "339227"
---
# <a name="store-inventory-management"></a>Správa skladových zásob

[!include [banner](includes/banner.md)]

Toto téma popisuje typy dokumentů, které můžete použít ke správě zásob.

Typy následující dokumentů slouží ke správě skladových zásob v organizaci.

Při práci se zásobami v aplikaci Dynamics 365 for Retail a používání aplikace Retail POS je důležité poznamenat, že POS poskytuje omezenou podporu pro dimenze zásob a určité typy skladových položek.  

Řešení POS nepodporuje následující konfigurace položek:
- Položky kusovníku (s výjimkou sady produktů, které používají některé součásti sady systému kusovníků)
- Položka se skutečnou hmotností
- Položky řízené dávkou

Aplikace Retail POS v současné době nepodporuje následující sledovací dimenze v POS:
- Dimenze dávkového sledování
- Dimenze vlastníka

Řešení POS poskytuje omezenou podporu následujících dimenzí. Omezená podpora označuje, že POS může nastavit některé z těchto dimenzí jako výchozí do skladových transakcí automaticky založených na konfiguraci nastavení skladu/úložiště. POS nebude plně podporovat dimenze způsobem, kterým jsou podporovány v případě ručního zadání prodejní transakce do ERP. 

- Místo konání
- Registrační značka (platí pouze v případě **procesů používání správy skladu** je povolena pro danou položku a sklad pro obchod)
- Sériové číslo
- Stav skladu

> [!NOTE]
> Všechny organizace musí otestovat konfigurace položky prostřednictvím POS při vývoji nebo v testovacím prostředí před nasazením do výroby. Položky otestujte provedením pravidelných hotovostních prodejních transakcí a vytvořením zákaznických objednávek (v příslušných případech) pomocí POS s položkami. Testování musí zahrnovat spuštění úplných procesů zaúčtování výkazů v testovacím prostředí a ověření, že nedochází k potížím.
> Konfigurace položek způsobem, který aplikace POS nepodporuje, bez řádného testování, může způsobit neúspěch procesu zaúčtování ve výrobě bez jednoduchého způsobu opravy problémů. Přizpůsobení aplikace partnerem nebo zákazníkem může být volitelně považováno za umožnění úspěšného dokončení těchto procesů zaúčtování. Pokud nejsou potřeba přizpůsobení, musí organizace zajistit, že konfigurace produktu byla provedena způsobem, který podporují standardní procesy aplikace POS/vytvoření objednávky/zaúčtování výkazu.

## <a name="purchase-orders"></a>Nákupní objednávky

Nákupní objednávky se vytvářejí v ústředí. Pokud je maloobchodní sklad zahrnut v záhlaví nákupní objednávky, objednávku lze přijmout v obchodě pomocí řešení Modern POS (MPOS) nebo Cloud POS v aplikaci Microsoft Dynamics 365 for Retail. Po zadání množství, která jsou přijata v obchodě, mohou být tato množství místně uložena pro další úpravy. Množství lze také potvrdit a odeslat do ústředí. V ústředí se množství, které bylo přijato v obchodě, zobrazuje v aplikaci Dynamics 365 for Retail, v poli **Přijmout nyní** v nákupní objednávce.

## <a name="transfer-orders"></a>Převodní příkazy

Převodní příkaz může stanovit, že určitý obchod je místo, ze kterého mohou být položky expedovány. V tomto případě se převodní příkaz zobrazí v obchodě jako požadavek vyskladnění v MPOS nebo Cloud POS. Jakmile jsou požadovaná množství vyskladněna, jsou potvrzena a odeslána do ústředí. V ústředí se množství, které bylo vyzvednuto v obchodě, zobrazuje v aplikaci Dynamics 365 for Retail, v poli **Expedovat nyní** v objednávce převodu. Převodní příkaz může stanovit, že určitý obchod je místo, do kterého mohou být položky expedovány. V tomto případě se převodní příkaz zobrazí v obchodě jako příjmová žádanka v MPOS nebo Cloud POS. Po zadání množství, která jsou přijata v obchodě, mohou být tato množství místně uložena pro další úpravy. Množství lze také potvrdit a odeslat do ústředí. V ústředí se množství, které bylo přijato v obchodě, zobrazuje v aplikaci Dynamics 365 for Retail, v poli **Přijmout nyní** v objednávce převodu.

## <a name="stock-counts"></a>Počty na skladě

Inventury mohou být plánované nebo neplánované. Plánované inventury zahajuje ústředí, které také určuje, které položky musí být spočítány. Ústředí vytvoří dokument inventury skladu, který lze přijmout v obchodě, kde jsou množství skutečných zásob na skladě zadána v MPOS nebo Cloud POS. Neplánované maloobchodní inventury jsou zahájeny v obchodě a množství skutečných zásob na skladě jsou aktualizována v MPOS nebo Cloud POS. Na rozdíl od plánovaných maloobchodních inventur nemají neplánované maloobchodní inventury předdefinovaný seznam položek. Po dokončení obou typů inventury budou potvrzeny a odeslány do ústředí. V ústředí bude inventura ověřena a zaúčtována.

## <a name="inventory-lookup"></a>Vyhledávání zásob

Na stránce vyhledávání zásob lze zobrazit aktuální množství produktu na skladě pro více obchodů a skladů. Kromě aktuálního množství na skladě je možné zobrazit budoucí množství, které lze slíbit (ATP) pro každý jednotlivý obchod. Chcete-li tak učinit, vyberte obchod, pro který chcete zobrazit ATP, a klikněte na **Zobrazit dostupnost obchodu**.
