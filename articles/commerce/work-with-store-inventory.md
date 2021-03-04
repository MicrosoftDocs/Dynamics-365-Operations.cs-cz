---
title: Správa skladových zásob
description: Toto téma popisuje typy dokumentů, které můžete použít ke správě zásob.
author: rubencdelgado
manager: AnnBe
ms.date: 05/15/2020
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
ms.openlocfilehash: a3e6450c358d12dc62c2ffa20e7ff529be86bbe5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410797"
---
# <a name="store-inventory-management"></a>Správa skladových zásob

[!include [banner](includes/banner.md)]

Při práci s inventářem v Microsoft Dynamics 365 Commerce a používání Point of Sale (POS) aplikací, je důležité si uvědomit, že POS poskytuje omezenou podporu pro některé dimenze inventáře a některé typy položek inventáře. Aplikace POS nepodporuje úplnou škálu možností konfigurace položek, které jsou k dispozici prostřednictvím možností konfigurace položek v Dynamics 365 Supply Chain Management.

Řešení POS v současné době nepodporuje následující rozměry produktu a konfigurace položek:

- Konfigurace rozměru produktu a položek kusovníku (kromě kusovníku, který používá některé součásti rozhraní kusovníku)
- Položka se skutečnou hmotností
- Položky řízené rozměrem produktu

Aplikace Retail POS v současné době nepodporuje následující sledovací dimenze v POS:

- Dimenze dávkového sledování
- Dimenze vlastníka

POS poskytuje omezenou podporu následujících dimenzí. Jinými slovy POS může nastavit některé z těchto dimenzí jako výchozí ve skladových transakcích podle na konfigurace skladu nebo úložiště. POS nebude plně podporovat dimenze způsobem, kterým jsou podporovány v případě ručního zadání prodejní transakce v Comerce Headquarters. 

- **Umístění skladu** - Když používají nové POS operace [Příchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) a [Odchozí operace ](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), uživatelé si mohou vybrat umístění inventáře skladu, ze kterého budou přijímat položky nebo odesílat položky odchozích objednávek. Pokud používají zastaralé operace **Vyzvednutí a příjem** pro příjem a odesílání odchozích převodů, je k dispozici omezená podpora správy polohy. Tato podpora je k dispozici pouze pokud **Použít procesy řízení skladu** byla pro položku a sklad obchodu zapnuta možnost. Místo inventáře nelze v současné době použít s operacemi **Počet na skladě** nebo **Vyhledávání zásob**.
- **Registrační značka** - Registrační značky platí pouze v případě, když byla povolena možnost **Použít procesy řízení skladu** pro danou položku a sklad obchodu. V POS, pokud je inventář přijat do skladu pomocí operace **Příchozí operace** nebo **Výdej a příjem**, kde byl zapnut proces správy skladu, a pokud je místo, které bylo vybráno pro příjem položky, spojeno s profilem místa, který vyžaduje kontrolu poznávací značky, aplikace POS systematicky aplikuje poznávací značku na řádek příjmu. Uživatelé POS nemohou tato data poznávací značky změnit ani spravovat. Je-li vyžadována úplná správa registračních značek, doporučujeme, aby obchod použil [skladovací aplikaci](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app) klienta účetního systému ke správě příjmu těchto položek.
- **Sériové číslo** – Aplikace POS má omezenou podporu pro jednotlivá sériová čísla, která mají být registrována na řádku prodejní transakce pro objednávky vytvořené v POS a obsahují serializované položky. Toto sériové číslo není ověřováno proti registrovaným sériovým číslům, která jsou již v zásobách. Je-li prodejní objednávka vytvořena v kanálu kontaktního střediska nebo splněna prostřednictvím podnikových zdrojů plánování (ERP) a více sériových čísel je registrováno v jednom řádku prodeje v průběhu procesu plnění v ERP, tato sériová čísla nebude možné použít nebo ověřit, pokud je pro tuto objednávku zpracováváno vrácení v POS. Když je inventář přijat pomocí operace **Příchozí operace**, uživatelé mohou [zaregistrovat nebo potvrdit přijatá sériová čísla](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items).
- **Stav zásob** - Pro položky, které používají proces řízení skladu a vyžadují stav zásob, nelze toto pole stavu v aplikaci POS nastavit nebo změnit. Výchozí stav zásob definovaný v konfiguraci skladu obchodu bude použit při příjmu položek do zásob.

> [!NOTE]
> Všechny organizace musí otestovat konfigurace položky prostřednictvím POS při vývoji nebo v testovacím prostředí před nasazením těchto konfigurací položek do produkčních prostředí. Položky otestujte používáním jich pro pravidelné hotovostní prodejní transakce a vytvořením zákaznických objednávek (v příslušných případech) pomocí POS s položkami. Před nasazením jakékoli nové konfigurace položek byste také měli otestovat plnění POS a procesy inventáře (například operace přijímání zásob a plnění objednávek), abyste se ujistili, že je aplikace POS podporuje. Testování musí zahrnovat spuštění úplného procesu účtování výkazů v testovacím prostředí a ověření, že při vytváření objednávek na tyto položky a jejich zveřejňování v commerce Headquarters nedochází k problémům.
>
> Pokud jsou položky nakonfigurovány tak, že je aplikace POS nepodporuje a není provedeno odpovídající testování, může se během procesu vytváření objednávek vyskytnout selhání dat, které nelze snadno opravit nebo které nejsou pokryty standardní podporou produktu.

## <a name="purchase-orders"></a>Nákupní objednávky

Objednávky jsou vytvářeny v commerce Headquarters. Pokud je sklad zahrnut v záhlaví nákupní objednávky nebo v řádku nákupní objednávky, objednávku lze přijmout v obchodě pomocí operace [Příchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) v POS. 

## <a name="transfer-orders"></a>Převodní příkazy

Převodní příkazy lze vytvořit v Commerce Headquarters nebo prostřednictvím operací [Příchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) nebo [Odchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) v POS. Použijte **Příchozí operace** operaci POS k vytvoření požadavku na převod, aby byl inventář odeslán do obchodu z jiného skladu nebo umístění obchodu. Použijte **Odchozí operace** operaci POS k vytvoření požadavku na převod, aby byl inventář odeslán z obchodu do jiného skladu nebo umístění obchodu. Po vytvoření příkazu k převodu do obchodu může tento obchod spravovat příjem inventáře pro příkaz k převodu prostřednictvím operace **Příchozí operace** v POS. Pokud je v obchodě dodávka zásob na jiné místo, operace **Odchozí operace** v POS se používá ke správě procesu odeslání tohoto obchodu.

## <a name="stock-counts"></a>Počty na skladě

Inventury mohou být plánované nebo neplánované. Plánované počty zásob se vytvářejí prostřednictvím centrály obchodu vytvořením dokumentu deníku Inventura, který je propojen se skladem obchodu. Tento deník určuje položky, které musí být spočítány. Obchod pak může přistupovat k těmto předdefinovaným inventurním deníkům a jednat podle nich pomocí operace **Počet na skladě** v POS. Uživatelé obchodu zahájí neplánovaný počet zásob, jak je požadováno, když použijí operaci **Počet na skladě** v POS. Na rozdíl od plánovaných maloobchodních inventur nemají neplánované maloobchodní inventury předdefinovaný seznam položek. Po dokončení obou typů inventury budou potvrzeny v POS a odeslány do ústředí. V ústředí musí být počet poté potvrzen a zaúčtován v Commerce Headquarters jako samostatný krok.

## <a name="inventory-lookup"></a>Vyhledávání zásob

Na stránce **Vyhledávání zásob** lze zobrazit aktuální množství produktu na skladě pro více obchodů a skladů. Kromě aktuálního množství na skladě je možné zobrazit budoucí množství, které lze slíbit (ATP) pro každý jednotlivý obchod. Vyberte obchod, pro který chcete zobrazit množství dostupném pro slíbení, a pak vyberte **Zobrazit dostupnost obchodu**. Informace o dostupných konfiguračních možnostech naleznete v části [Výpočet dostupnosti zásob pro maloobchodní kanály](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).


[!INCLUDE[footer-include](../includes/footer-banner.md)]