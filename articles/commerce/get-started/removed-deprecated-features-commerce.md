---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Commerce
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Commerce.
author: josaw
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 5544fefbbf0dfc012e868b672f80cc2be30fe7ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020855"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Commerce.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování. 

> [!NOTE]
> Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](/dynamics/s-e/). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.17

### <a name="full-dataset-generation-interval-is-deprecated"></a>Interval generování celé datové sady je zastaralý

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Počínaje tímto vydáním, ve formuláři **Parametry plánovače obchodu** v centrále Dynamics 365 bude pole **Celý interval generování datové sady ve dnech** zastaralé. Počínaje touto verzí bude pole vizuálně odstraněno, takže hodnotu nebude možné upravit. Zůstane jako hodnota **0**. |
| **Nahrazeno jinou funkcí?**   | Žádný |
| **Ovlivněné oblasti produktu**         | Dynamics 365 Commerce |
| **Možnost nasazení**              | Vše|
| **Stav**                         | Zastaralé. Toto pole nepoužívejte ani v něm neměňte hodnotu.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Podpora aplikace Internet Explorer 11 pro Dynamics 365 je zastaralá

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | S platností od prosince 2020 je podpora aplikace Microsoft Internet Explorer 11 zastaralá pro všechny produkty Dynamics 365 a Internet Explorer 11 nebude podporován po srpnu 2021.<br><br>To bude mít dopad na zákazníky, kteří používají produkty Dynamics 365, které jsou navrženy pro použití prostřednictvím rozhraní Internet Explorer 11. Po srpnu 2021 nebude Internet Explorer 11 podporován pro takové produkty Dynamics 365. |
| **Nahrazeno jinou funkcí?**   | Doporučujeme zákazníkům přejít na Microsoft Edge.|
| **Ovlivněné oblasti produktu**         | Všechny produkty Dynamics 365 |
| **Možnost nasazení**              | Vše|
| **Stav**                         | Zastaralé. Internet Explorer 11 nebude podporován po srpnu 2021.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.11
### <a name="data-action-hooks"></a>Zavěšení datových akcí
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Funkce háčků datových akcí byla zastaralá kvůli problémům s výkonem. |
| **Nahrazeno jinou funkcí?**   | Doporučujeme použít [přepisy akce dat](../e-commerce-extensibility/data-action-overrides.md) ke změně obchodní logiky ve vrstvě akce dat.|
| **Ovlivněné oblasti produktu**         | Akce dat rozšiřitelnosti elektronického obchodování |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: k verzi 10.0.11 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Maloobchodní podpora SDK pro Visual Studio 2015, msbuild 14.0 a Retail SDK\Referenční knihovny a nástroje
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Maloobchodní podpora SDK pro Visual Studio 2015 byla vyřazena a aktualizována tak, aby podporovala VS 2017, msbuild 15.0 a všechny referenční knihovny a nástroje komerčního generátoru proxy ve složce RetailSDK\References přesunuty do balíčků NuGet ke zjednodušení modelu rozšíření a procesu upgradu SDK.|
| **Nahrazeno jinou funkcí?**   | Doporučujeme vám řídit se při aktualizaci systému řídit informacemi v části [Migrace sady Retail SDK z Visual Studio 2015 na Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md). |
| **Ovlivněné oblasti produktu**         | Maloobchodní rozšíření SDK |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: k verzi 10.0.11 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Maloobchodní rozšíření serveru pomocí IEdmModelExtender a CommerceController
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Rozšíření Retail serveru pomocí IEdmModelExtender a CommerceController bylo vyřazeno, aby poskytovalo zjednodušený model rozšíření. Nová implementace bude mít pouze třídu kontrolerů bez další implementace třídy IEdmModelExtender. Tím se také vyhnete závislosti na konkrétní verzi OData (pokud je aktualizována verze OData, může to poškodit rozšíření). |
| **Nahrazeno jinou funkcí?**   |  Doporučujeme použít model rozšíření třídy IController importováním balíčku NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Ovlivněné oblasti produktu**         | Rozšíření serveru Retail Server |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: k verzi 10.0.11 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Rozšíření hardwarové stanice pomocí IHardwareStationController
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Rozšíření hardwarové stanice pomocí IHardwareStationController bylo vyřazeno, aby se získal zjednodušený model rozšíření. Nová implementace bude mít pouze třídu IController bez jakékoli další implementace třídy a aby se předešlo závislosti na knihovnách základních hardwarových stanic, musí předchozí rozšíření odkazovat na více knihoven.) |
| **Nahrazeno jinou funkcí?**   | Doporučuje se použít model rozšíření třídy IController importováním balíčku NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Ovlivněné oblasti produktu**         | Rozšíření hardwarové stanice |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: k verzi 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.10
### <a name="pos-operation-803---picking-and-receiving"></a>Operace POS 803 – Vyzvednutí a příjem
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Operace stahování a přijímání jsou zastaralé kvůli novému přepracování operací. |
| **Nahrazeno jinou funkcí?**   | Ano. Je nahrazen dvěma novými operacemi POS: příchozí operace (804) a odchozí operace (805).|
| **Ovlivněné oblasti produktu**         | Aplikace Pokladní místo (POS) |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Od vydání 10.0.10 již operace vyzvednutí a přijetí nebude mít žádné nové aktualizace funkcí. V budoucích verzích budou pro tuto operaci provedeny pouze kritické opravy chyb. Doporučuje se, aby všichni zákazníci přešli na nové [příchozí operace](../pos-inbound-inventory-operation.md) a [odchozí operace](../pos-outbound-inventory-operation.md), které budou nadále součástí našeho dlouhodobého přehledu aplikací. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.7
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Rozhraní API obchodu GetProductAvailabilities a GetAvailableInventoryNearby
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Byla vytvořena nová optimalizovaná rozhraní API nahrazující rozhraní API GetProductAvailabilities a GetAvailableInventoryNearby. |
| **Nahrazeno jinou funkcí?**   | Ano: Nahrazuje je rozhraní API GetEstimatedAvailability a GetEstimatedProductWarehouseAvailability. |
| **Ovlivněné oblasti produktu**         | Sada SDK pro elektronický obchod |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Ukončeno: Od vydání 10.0.7 nebudou investovány žádné technické prostředky do rozhraní API GetProductAvailabilities a GetAvailableInventoryNearby. Organizace, které používají tato API ve svých implementacích elektronického obchodování, by měly přejít na nová rozhraní API GetEstimatedAvailability a GetEstimatedProductWarehouseAvailability a povolit [Funkci pro optimalizaci dostupnosti produktu](../calculated-inventory-retail-channels.md).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Předchozí oznámení o odebraných nebo zastaralých funkcích
Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]