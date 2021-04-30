---
title: Konfigurace DPH pro online objednávky
description: Tohle téma poskytuje přehled o výběru skupiny DPH pro různé typy online objednávek v Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8df939c1a566fb63bc53e455cc6c2aa85956ac79
ms.sourcegitcommit: 583801af75c50915ea5ffc60e831fb617d045533
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853804"
---
# <a name="configure-sales-tax-for-online-orders"></a>Konfigurace DPH pro online objednávky

[!include [banner](includes/banner.md)]

Toto téma poskytuje přehled výběru skupiny DPH pro různé typy online objednávek pomocí nastavení daně založené na cílovém nebo zákaznickém účtu. 

Pro svůj kanál elektronického obchodování možná bude chtít podporu možností, jako je doručení nebo vyzvednutí online objednávek. Uplatnění DPH závisí na možnosti vybrané vašimi online zákazníky. 

## <a name="destination-based-taxes-for-online-orders"></a>Daně založené na cíli pro online objednávky

Obecně jsou daně u online objednávek, které jsou dodávány na adresy zákazníků, definovány podle cílového místa. Každá skupina DPH má konfiguraci daně na základě cílového místa maloobchodu, ve které může vaše firma v hierarchické podobě definovat podrobnosti o cílovém místě, jako je země nebo oblast, stát, kraj a město.

### <a name="orders-delivered-to-customer-address"></a>Objednávky dodané na adresu zákazníka

Když je zadána online objednávka, daňový modul Commerce použije dodací adresu každé řádkové položky v objednávce a vyhledá skupiny DPH s odpovídajícími cílovými daňovými kritérii. Například u online objednávky s dodací adresou řádkové položky do San Franciska v Kalifornii vyhledá daňový modul skupinu DPH a kód DPH pro Kalifornii a poté odpovídajícím způsobem vypočítá daň pro každou řádkovou položku.

### <a name="order-pick-up-in-store"></a>Vyzvednutí objednávky v obchodě

U řádků objednávky se zadaným vyzvednutím v obchodě nebo pouličním výdejem se použije daňová skupina z vybraného obchodu pro vyzvednutí. Podrobnosti, jak nastavit DPH pro daný obchod, viz [Nastavení dalších daňových možností pro obchody](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

## <a name="customer-account-based-taxes-for-online-orders"></a>Daně založené na zákazníkovi pro online objednávky

Může nastat obchodní scénář, kdy chcete nakonfigurovat skupinu DPH na konkrétním zákaznickém účtu v centrále Commerce. V centrále jsou dvě místa, kde můžete nakonfigurovat DPH na zákaznickém účtu. Abyste k nim měli přístup, musíte se nejprve dostat na stránku s údaji o zákazníkovi přechodem na **Maloobchod a obchod \> Zákazníci \> Všichni zákazníci** a poté vyberte zákazníka.

Dvě místa, kde můžete nakonfigurovat DPH na zákaznickém účtu, jsou:

- **Skupina DPH** na rychlé kartě **Faktura a dodání** na stránce s podrobnostmi o zákazníkovi. 
- **DPH** na rychlé kartě **Všeobecné** na stránce **Spravovat adresy**. Chcete-li se tam dostat ze stránky s podrobnostmi o zákazníkovi, vyberte konkrétní adresu pod rychlou kartou **Adresy** a poté vyberte **Pokročilé**.

> [!TIP]
> Pokud chcete u online objednávek zákazníků uplatnit pouze daně podle místa určení a vyhnout se daním na základě účtu zákazníka, ujistěte se, že pole **Skupina DPH** je prázdné na rychlé kartě **Faktura a dodání** na stránce s podrobnostmi o zákazníkovi. Abyste zajistili, že noví zákazníci, kteří se zaregistrují pomocí online kanálu, nezdědí nastavení skupiny DPH z výchozího nastavení zákazníka nebo skupiny zákazníků, ujistěte se, že pole **Skupina DPH** je také prázdné pro výchozí nastavení zákazníka online kanálu a nastavení skupiny zákazníků (**Maloobchod a obchod \> Zákazníci \> Skupiny zákazníků**).

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Určete použitelnost daně podle místa určení nebo daně podle účtu zákazníka 

V následující tabulce je vysvětleno, zda se u online objednávek aplikují daně na základě cíle, nebo daně na základě účtu zákazníka. 

| Typ zákazníka | Dodací adresa                   | Zákazník > Faktura a dodání > Skupina DPH? | Adresa na zákaznickém účtu v centrále? | Adresa zákazníka > Pokročilé > Obecné > Skupina DPH?                                              | Použitá skupina DPH      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Host         | Manhattan, NY                      | Ne (prázdné)                                                | Ne (prázdné)                              | Ne (prázdné)                                                                                                   | NY (daně podle místa určení) |
| Přihlášeni     | Austin, TX                          | Ne (prázdné)                                             | Ano                               | Není<br/><br/>Nová adresa přidána prostřednictvím online kanálu.                                                            | TX (daně podle místa určení) |
| Přihlášeni     | San Francisco, CA (vyzvednutí v obchodě) | Ano (NY)                                            | Nelze použít                              | Nelze použít                                                                                                    | CA (daně podle místa určení) |
| Přihlášeni     | Houston, TX                         | Ano (NY)                                            | Ano                               | Ano (NY)<br/><br/>Nová adresa přidaná prostřednictvím online kanálu a skupiny DPH zděděné z účtu zákazníka. | NY (daně podle účtu zákazníka)  |
| Přihlášeni     | Austin, TX                          | Ano (NY)                                            | Ano                               | Ano (NY)<br/><br/>Nová adresa přidaná prostřednictvím online kanálu a skupiny DPH zděděné z účtu zákazníka. | NY (daně podle účtu zákazníka)  |
| Přihlášeni     | Sarasota, FL                       | Ano (NY)                                            | Ano                               | Ano (WA)<br/><br/>Ručně nastaveno na WA.                                                                          | WA (daně podle účtu zákazníka)  |
| Přihlášeni     | Sarasota, FL                       | Ne (prázdné)                                                | Ano                               | Ano (WA)<br/><br/>Ručně nastaveno na WA.                                                                          | WA (daně podle účtu zákazníka)  |

## <a name="additional-resources"></a>Další prostředky

[Nastavení daní pro online obchody podle cílového místa](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[Přehled DPH](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Metody výpočtu DPH v poli Zdroj](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[ Přiřazení a přepsání DPH](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Možnosti výpočtu celé částky a intervalu pro kódy daně z prodeje](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Výpočet osvobození od daně](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
