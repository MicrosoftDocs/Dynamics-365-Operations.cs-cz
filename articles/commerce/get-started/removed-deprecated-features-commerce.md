---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Commerce
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Commerce.
author: josaw
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b582b8b95fcf2ad45aa1bb49eb5594d30874e0f4
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559552"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Commerce.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování. 

> [!NOTE]
> Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](/dynamics/s-e/). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.21

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Nastavení zpracování překrývajících se slev v parametrech Commerce

Nastavení **Zpracování překrývajících se slev** na stránce **Parametry Commerce** je ve verzi Commerce 10.0.21 označeno jako zastaralé. Do budoucna bude cenový modul Commerce používat jeden algoritmus k určení optimální kombinace překrývajících se slev.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | <p>Nastavení **Zpracování překrývajících se slev** v parametrech Commerce řídí, jak cenový modul Commerce vyhledává a určuje optimální kombinaci překrývajících se slev. Aktuálně nabízí tři možnosti:<p><ul><li> **Nejlepší výkon** – Tato možnost používá pokročilý heuristický algoritmus a metodu [mezní hodnota pořadí](../optimal-combination-overlapping-discounts.md) k včasnému určení priorit, vyhodnocení a stanovení nejlepší kombinace slev.</li><li>**Vyvážený výpočet** – V aktuálním kódu tato možnost funguje stejně jako možnost **Nejlepší výkon**. Je to tedy v podstatě duplicitní možnost.</li><li>**Vyčerpávající výpočet** – Tato možnost používá starý algoritmus, který během výpočtu ceny prochází všemi možnými kombinacemi slev. U objednávek, které mají velký počet řádků a rozsáhlá množství, může tato možnost způsobit zpomalení výpočtu.</li></ul><p>Abychom zjednodušili konfiguraci, zlepšili výkon a omezili incidenty způsobené starým algoritmem, nastavení **Zpracování překrývajících se slev** zcela odstraníme a aktualizujeme interní logiku cenového modulu Commerce tak, aby nyní používal pouze pokročilý algoritmus (tj. algoritmus možnosti **Nejlepší výkon**).</p> |
| **Nahrazeno jinou funkcí?**   | Ne. Doporučujeme organizacím, které používají možnost **Vyvážený výpočet** nebo **Vyčerpávající výpočet**, přepnout před odstraněním této funkce na **Nejlepší výkon**. |
| **Ovlivněné oblasti produktu**         | Tvorba cen a slevy |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Od vydání 10.0.21 bude nastavení **Zpracování překrývajících se slev** z parametrů Commerce odstraněno v říjnu 2022. |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>Maloobchodní SDK distribuovaná pomocí Lifecycle Services

Retail SDK se dodává ve službě Lifecycle Services (LCS). Tento způsob distribuce je ve verzi 10.0.21 zastaralý. Do budoucna budou referenční balíčky Retail SDK, knihovny a ukázky publikovány ve veřejných úložištích na GitHubu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Retail SDK se dodává v LCS. Dokončení procesu LCS trvá několik hodin a tento postup je nutné opakovat pro každou aktualizaci. Do budoucna budou referenční balíčky Retail SDK, knihovny a ukázky publikovány ve veřejných úložištích na GitHubu. Ukázky rozšíření a referenční balíčky lze snadno spotřebovat a aktualizace se dokončí za několik minut. |
| **Nahrazeno jinou funkcí?**   |  [Stažení ukázek Retail SDK a referenčních balíčků z GitHub a NuGet](../dev-itpro/retail-sdk/sdk-github.md) |
| **Ovlivněné oblasti produktu**         | Retail SDK |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Od verze 10.0.21 bude sada SDK dodávaná prostřednictvím virtuálních počítačů LCS v říjnu 2022 odstraněna. |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>Maloobchodně nasaditelný balíček a kombinované instalační programy POS, hardwarové stanice a cloudové škály

Maloobchodní nasazitelné balíčky generované pomocí Retail SDK MSBuild jsou v 10.0.21 zastaralé. Do budoucna použijte balíček Cloud Scale Unit (CSU) pro rozšíření Cloud Scale Unit (Commerce Runtime, databáze kanálů, bezobslužné obchodní API, platby a cloudové prodejní místo (POS)). Použijte instalační programy pouze pro rozšíření pro POS, hardwarovou stanici a cloudovou jednotku, kterou hostujete sami.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Retail nasaditelný balíček je kombinovaný balíček, který obsahuje kompletní sadu rozšiřujících balíčků a instalačních programů. Tento kombinovaný balíček komplikuje nasazení, protože rozšíření CSU přecházejí na Cloud scale unit a instalátory jsou nasazeny v obchodech. Instalační programy obsahují rozšíření a základní produkt, což ztěžuje aktualizace. Při každém upgradu je zapotřebí sloučení kódu a generování balíčku. Aby se tento proces zjednodušil, balíčky rozšíření jsou nyní rozděleny na komponenty pro snadné nasazení a správu. S novým přístupem jsou rozšíření a instalační programy základních produktů odděleny a lze je nezávisle obsluhovat a upgradovat bez sloučení kódu nebo přebalování.|
| **Nahrazeno jinou funkcí?**   | Rozšíření CSU, instalátory rozšíření POS, instalační programy rozšíření hardwarových stanic |
| **Ovlivněné oblasti produktu**         | Rozšíření a nasazení Dynamics 365 Commerce |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Od vydání 10.0.21 bude podpora pro nasazení RetailDeployablePackage v LCS v říjnu 2022 odstraněna. |

Další informace naleznete zde:

+ [Vygenerujte samostatný balíček pro Commerce Cloud Scale Unit (CSU)](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [Vytvoření balíčku rozšíření Modern POS](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [Integrace POS s novým hardwarovým zařízením](../dev-itpro/hardware-device-extension.md)
+ Vzorky kódu
    + [Cloud Scale Unit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [POS, CSU a Hardwarová stanice](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln a CloudPOs.sln v sadě Retail SDK

Vývoj rozšíření POS pomocí ModernPos.sln, CloudPOs.sln, POS.Extension.csproj a složky POS je ve verzi 10.0.21 zastaralý. Do budoucna použijte pro rozšíření POS balíčky SDK nezávislé na POS.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | V dřívějších verzích sady Retail SDK, pokud existují rozšíření POS, je k aktualizaci na nejnovější verzi POS potřeba sloučení kódu a přebalení. Sloučení kódu byl časově náročný proces upgradu a museli jste v úložišti udržovat úplnou sadu Retail SDK. Také jste museli zkompilovat základní projekt POS.App. Použitím nezávislého modelu balení musíte udržovat pouze své rozšíření. Proces aktualizace na nejnovější verzi rozšíření POS je stejně snadný jako aktualizace verze balíčku NuGet, který váš projekt spotřebuje. Rozšíření lze nasadit nezávisle a služby používají instalační programy rozšíření. Základní POS lze nasadit a udržovat samostatně a není nutné sloučení kódu ani přebalení základního instalačního programu nebo kódu. |
| **Nahrazeno jinou funkcí?**   | [Balení SDK nezávislé na POS](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Ovlivněné oblasti produktu**         | Rozšíření a nasazení Dynamics 365 Commerce POS |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Od verze 10.0.21 bude v říjnu 2022 odebrána podpora pro kombinované POS balíčky a model rozšíření využívající ModernPos.Sln, CloudPOs.sln a POS.Extensons.csproj v Retail SDK. |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.17

### <a name="full-dataset-generation-interval-is-deprecated"></a>Interval generování celé datové sady je zastaralý

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Počínaje tímto vydáním, ve formuláři **Parametry plánovače obchodu** v centrále Dynamics 365 bude pole **Celý interval generování datové sady ve dnech** zastaralé. Počínaje touto verzí bude pole vizuálně odstraněno, takže hodnotu nebude možné upravit. Zůstane jako hodnota **0**. |
| **Nahrazeno jinou funkcí?**   | Žádný |
| **Ovlivněné oblasti produktu**         | Dynamics 365 Commerce |
| **Možnost nasazení**              | Vše|
| **Stav**                         | Zastaralé. Toto pole nepoužívejte ani v něm neměňte hodnotu.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Podpora aplikace Internet Explorer 11 pro Dynamics 365 je zastaralá

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | S platností od prosince 2020 je aplikace Microsoft Internet Explorer 11 označena jako zastaralá u všech produktů Dynamics 365 a Internet Explorer 11 nebude po srpnu 2021 podporován.<br><br>To bude mít dopad na zákazníky, kteří používají produkty Dynamics 365, které jsou navrženy pro použití prostřednictvím rozhraní Internet Explorer 11. Po srpnu 2021 nebude Internet Explorer 11 podporován pro takové produkty Dynamics 365. |
| **Nahrazeno jinou funkcí?**   | Doporučujeme zákazníkům přejít na Microsoft Edge.|
| **Ovlivněné oblasti produktu**         | Všechny produkty Dynamics 365 |
| **Možnost nasazení**              | Vše|
| **Stav**                         | Zastaralé. Internet Explorer 11 nebude po srpnu 2021 podporován.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.11
### <a name="data-action-hooks"></a>Zavěšení datových akcí
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Funkce háčků datových akcí byla zastaralá kvůli problémům s výkonem. |
| **Nahrazeno jinou funkcí?**   | Doporučujeme použít [přepisy akce dat](../e-commerce-extensibility/data-action-overrides.md) ke změně obchodní logiky ve vrstvě akce dat.|
| **Ovlivněné oblasti produktu**         | Akce dat rozšiřitelnosti elektronického obchodování |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: k verzi 10.0.11 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Maloobchodní podpora SDK pro Visual Studio 2015, msbuild 14.0 a Retail SDK\Referenční knihovny a nástroje
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Maloobchodní podpora SDK pro Visual Studio 2015 byla vyřazena a aktualizována tak, aby podporovala VS 2017, msbuild 15.0 a všechny referenční knihovny a nástroje komerčního generátoru proxy ve složce RetailSDK\References přesunuty do balíčků NuGet ke zjednodušení modelu rozšíření a procesu upgradu SDK.|
| **Nahrazeno jinou funkcí?**   | Doporučujeme vám řídit se při aktualizaci systému řídit informacemi v části [Migrace sady Retail SDK z Visual Studio 2015 na Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md). |
| **Ovlivněné oblasti produktu**         | Maloobchodní rozšíření SDK |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: k verzi 10.0.11 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Maloobchodní rozšíření serveru pomocí IEdmModelExtender a CommerceController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Rozšíření Retail serveru pomocí IEdmModelExtender a CommerceController bylo vyřazeno, aby poskytovalo zjednodušený model rozšíření. Nová implementace bude mít pouze třídu kontrolerů bez další implementace třídy IEdmModelExtender. Tím se také vyhnete závislosti na konkrétní verzi OData (pokud je aktualizována verze OData, může to poškodit rozšíření). |
| **Nahrazeno jinou funkcí?**   |  Doporučujeme použít model rozšíření třídy IController importováním balíčku NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Ovlivněné oblasti produktu**         | Rozšíření serveru Retail Server |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: k verzi 10.0.11 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Rozšíření hardwarové stanice pomocí IHardwareStationController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Rozšíření hardwarové stanice pomocí IHardwareStationController bylo vyřazeno, aby se získal zjednodušený model rozšíření. Nová implementace bude mít pouze třídu IController bez jakékoli další implementace třídy a aby se předešlo závislosti na knihovnách základních hardwarových stanic, musí předchozí rozšíření odkazovat na více knihoven.) |
| **Nahrazeno jinou funkcí?**   | Doporučuje se použít model rozšíření třídy IController importováním balíčku NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Ovlivněné oblasti produktu**         | Rozšíření hardwarové stanice |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: k verzi 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.10
### <a name="pos-operation-803---picking-and-receiving"></a>Operace POS 803 – Vyzvednutí a příjem
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Operace stahování a přijímání jsou zastaralé kvůli novému přepracování operací. |
| **Nahrazeno jinou funkcí?**   | Ano. Je nahrazen dvěma novými operacemi POS: příchozí operace (804) a odchozí operace (805).|
| **Ovlivněné oblasti produktu**         | Aplikace Pokladní místo (POS) |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé: Od vydání 10.0.10 již operace vyzvednutí a přijetí nebude mít žádné nové aktualizace funkcí. V budoucích verzích budou pro tuto operaci provedeny pouze kritické opravy chyb. Doporučuje se, aby všichni zákazníci přešli na nové [příchozí operace](../pos-inbound-inventory-operation.md) a [odchozí operace](../pos-outbound-inventory-operation.md), které budou nadále součástí našeho dlouhodobého přehledu aplikací. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.7
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Rozhraní API obchodu GetProductAvailabilities a GetAvailableInventoryNearby
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Byla vytvořena nová optimalizovaná rozhraní API nahrazující rozhraní API GetProductAvailabilities a GetAvailableInventoryNearby. |
| **Nahrazeno jinou funkcí?**   | Ano: Nahrazuje je rozhraní API GetEstimatedAvailability a GetEstimatedProductWarehouseAvailability. |
| **Ovlivněné oblasti produktu**         | Sada SDK pro elektronický obchod |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Ukončeno: Od vydání 10.0.7 nebudou investovány žádné technické prostředky do rozhraní API GetProductAvailabilities a GetAvailableInventoryNearby. Organizace, které používají tato API ve svých implementacích elektronického obchodování, by měly přejít na nová rozhraní API GetEstimatedAvailability a GetEstimatedProductWarehouseAvailability a povolit [Funkci pro optimalizaci dostupnosti produktu](../calculated-inventory-retail-channels.md).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Předchozí oznámení o odebraných nebo zastaralých funkcích
Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
