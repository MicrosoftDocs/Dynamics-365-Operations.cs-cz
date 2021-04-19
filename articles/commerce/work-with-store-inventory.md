---
title: Správa skladových zásob
description: Toto téma popisuje typy dokumentů, které můžete použít ke správě zásob.
author: rubencdelgado
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c4891f9dcb031f4cb8dfb91f3fe1a301aad9838e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793866"
---
# <a name="commerce-inventory-management"></a>Správa zásob Commerce

[!include [banner](includes/banner.md)]

Když pracujete se zásobami v Microsoft Dynamics 365 Commerce a používáte jakoukoli z aplikací Commerce, které jsou připojeny ke Commerce Scale Unit (CSU), je důležité vědět, že logika zpracování objednávek v CSU poskytuje omezenou podporu pro některé dimenze zásob a některé typy skladových položek. Aplikace Commerce nepodporuje úplnou škálu možností konfigurace položek, které jsou k dispozici prostřednictvím možností konfigurace položek v Dynamics 365 Supply Chain Management.

Aplikace Commerce, které jsou spuštěny na CSU, v současné době nepodporují následující rozměry produktu a konfigurace položek:

- Konfigurace rozměru produktu a položek kusovníku (kromě kusovníku, který používá některé součásti rozhraní kusovníku)
- Položka se skutečnou hmotností
- Položky řízené rozměrem produktu

Aplikace Commerce, které jsou spuštěny na CSU, v současné době nepodporuje následující sledovací dimenze:
- Dimenze vlastníka

- Aplikace Pokladní místo (POS) může nabídnout omezenou podporu pro následující dimenze. POS může automaticky vložit některé z těchto dimenzí ve skladových transakcích na základě konfigurace nastavení skladu nebo obchodu. POS však nebude plně podporovat dimenze způsobem, kterým jsou podporovány v případě ručního zadání prodejní transakce v Comerce Headquarters. 

- **Umístění skladu** - Když používají nové POS operace [Příchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) a [Odchozí operace ](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), uživatelé si mohou vybrat umístění inventáře skladu, ze kterého budou přijímat položky nebo odesílat položky odchozích objednávek. Pokud používají zastaralé operace **Vyzvednutí a příjem** pro příjem a odesílání odchozích převodů, je k dispozici omezená podpora správy polohy. Tato podpora je k dispozici pouze pokud **Použít procesy řízení skladu** byla pro položku a sklad obchodu zapnuta možnost. Místo inventáře nelze v současné době použít s operacemi **Počet na skladě** nebo **Vyhledávání zásob**.

- **Registrační značka** - Registrační značky platí pouze v případě, když byla povolena možnost **Použít procesy řízení skladu** pro danou položku a sklad obchodu. V POS, pokud je inventář přijat do skladu pomocí operace **Příchozí operace** nebo **Výdej a příjem**, kde byl zapnut proces správy skladu, a pokud je místo, které bylo vybráno pro příjem položky, spojeno s profilem místa, který vyžaduje kontrolu poznávací značky, aplikace POS systematicky aplikuje poznávací značku na řádek příjmu. Uživatelé POS nemohou tato data poznávací značky změnit ani spravovat. Je-li vyžadována úplná správa registračních značek, doporučujeme, aby obchod použil [skladovací aplikaci](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app) klienta účetního systému ke správě příjmu těchto položek.

- **Sériové číslo** – Aplikace POS má omezenou podporu pro jednotlivá sériová čísla, která mají být registrována na řádku prodejní transakce pro objednávky vytvořené v POS a obsahují serializované položky. Toto sériové číslo není ověřováno proti registrovaným sériovým číslům, která jsou již v zásobách. Je-li prodejní objednávka vytvořena v kanálu kontaktního střediska nebo splněna prostřednictvím podnikových zdrojů plánování (ERP) a více sériových čísel je registrováno v jednom řádku prodeje v průběhu procesu plnění v ERP, tato sériová čísla nebude možné použít nebo ověřit, pokud je pro tuto objednávku zpracováváno vrácení v POS. Když je inventář přijat pomocí operace **Příchozí operace**, uživatelé mohou [zaregistrovat nebo potvrdit přijatá sériová čísla](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items).

- **ID šarže** - Aplikace POS poskytuje omezenou podporu během odesílání výpisů, pokud se prodává položka řízená dávkou, ale uživatelé POS nejsou schopni definovat ID dávky, které bylo prodáno nebo vybráno při použití aplikace POS.

- **Stav zásob** - Pro položky, které používají proces řízení skladu a vyžadují stav zásob, nelze toto pole stavu v aplikaci POS nastavit nebo změnit. Výchozí stav zásob definovaný v konfiguraci skladu obchodu bude použit při příjmu položek do zásob.

> [!NOTE]
> Všechny organizace musí otestovat konfigurace položky prostřednictvím aplikací Commerce při vývoji nebo v testovacím prostředí před nasazením těchto konfigurací položek do produkčních prostředí. Otestujte své položky a používejte je k provádění běžných prodejních transakcí cash-and-carry v POS a vytváření objednávek zákazníků (podle potřeby) prostřednictvím POS, kontaktního střediska nebo elektronického obchodování, abyste ověřili, že je lze plně podporovat. Před nasazením jakékoli nové konfigurace položek byste také měli otestovat plnění POS a procesy inventáře (například operace přijímání zásob a plnění objednávek), abyste se ujistili, že je aplikace POS podporuje. Testování musí zahrnovat spuštění úplného procesu účtování výkazů/objednávek v testovacím prostředí a ověření, že při vytváření objednávek na tyto položky a jejich zveřejňování v commerce Headquarters nedochází k problémům se zaúčtováním.
>
> Pokud jsou položky konfigurovány způsobem, který není podporován aplikacemi Commerce a neprovádí se příslušné testování, mohou nastat selhání dat, která se nedají snadno opravit nebo opravit vůbec nejdou.

## <a name="purchase-orders"></a>Nákupní objednávky

Objednávky jsou vytvářeny v commerce Headquarters. Pokud je sklad zahrnut v záhlaví nákupní objednávky nebo v řádku nákupní objednávky, objednávku lze přijmout v obchodě pomocí operace [Příchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) v POS. 

## <a name="transfer-orders"></a>Převodní příkazy

Převodní příkazy lze vytvořit v Commerce Headquarters nebo prostřednictvím operací [Příchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) nebo [Odchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) v POS. Použijte **Příchozí operace** operaci POS k vytvoření požadavku na převod, aby byl inventář odeslán do obchodu z jiného skladu nebo umístění obchodu. Použijte **Odchozí operace** operaci POS k vytvoření požadavku na převod, aby byl inventář odeslán z obchodu do jiného skladu nebo umístění obchodu. Po vytvoření příkazu k převodu do obchodu může tento obchod spravovat příjem inventáře pro příkaz k převodu prostřednictvím operace **Příchozí operace** v POS. Pokud je v obchodě dodávka zásob na jiné místo, operace **Odchozí operace** v POS se používá ke správě procesu odeslání tohoto obchodu.

## <a name="stock-counts"></a>Počty na skladě

Inventury mohou být plánované nebo neplánované. Plánované počty zásob se vytvářejí prostřednictvím centrály obchodu vytvořením dokumentu deníku Inventura, který je propojen se skladem obchodu. Tento deník určuje položky, které musí být spočítány. Obchod pak může přistupovat k těmto předdefinovaným inventurním deníkům a jednat podle nich pomocí operace **Počet na skladě** v POS. Uživatelé obchodu zahájí neplánovaný počet zásob, jak je požadováno, když použijí operaci **Počet na skladě** v POS. Na rozdíl od plánovaných maloobchodních inventur nemají neplánované maloobchodní inventury předdefinovaný seznam položek. Po dokončení obou typů inventury budou potvrzeny v POS a odeslány do ústředí. V ústředí musí být počet poté potvrzen a zaúčtován v Commerce Headquarters jako samostatný krok.

## <a name="inventory-lookup"></a>Vyhledávání zásob

Na stránce **Vyhledávání zásob** lze zobrazit aktuální množství produktu na skladě pro více obchodů a skladů. Kromě aktuálního množství na skladě je možné zobrazit budoucí množství, které lze slíbit (ATP) pro každý jednotlivý obchod. Vyberte obchod, pro který chcete zobrazit množství dostupném pro slíbení, a pak vyberte **Zobrazit dostupnost obchodu**. Informace o dostupných konfiguračních možnostech naleznete v části [Výpočet dostupnosti zásob pro maloobchodní kanály](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).


[!INCLUDE[footer-include](../includes/footer-banner.md)]