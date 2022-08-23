---
title: Preview verze Dynamics 365 Commerce 10.0.29 (říjen 2022)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Commerce 10.0.29.
author: josaw1
ms.date: 08/02/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c1f85fcd8f79106a3af93489d3bef608b9840bf3
ms.sourcegitcommit: 91f58a9863f4e8f30ac787c2a9771c1ff6a05f72
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/03/2022
ms.locfileid: "9224231"
---
# <a name="preview-of-dynamics-365-commerce-10029-october-2022"></a>Preview verze Dynamics 365 Commerce 10.0.29 (říjen 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tento článek uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Commerce verze Preview 10.0.29. Tato verze má číslo sestavení 10.0.1326 a je k dispozici podle následujícího plánu:

- **Preview verze:** Srpen 2022
- **Obecně dostupné vydání (automatická aktualizace):** Září 2022
- **Obecně dostupné vydání (automatická aktualizace):** Říjen 2022

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Tento článek můžeme aktualizovat, aby obsahoval funkce, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Oblast funkce | Funkce | Další informace | Povolil/a |
|---------|------------------|----------------|--------------| 
| B2B | [Aktivace podpory prodejních smluv napříč kanály](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | Tato funkce umožňuje organizacím prodejců typu business-to-business (B2B) používat prodejní smlouvy v Commerce headquarters k definování smluvních cen pro své kupující. Když kupující B2B nakupuje na webu elektronického obchodu, smluvní ceny, které jsou nakonfigurovány pro kupující organizaci B2B, se automaticky použijí na celý proces objevování, nákupu a pokladny. | Správa funkcí<p>*Podpora prodejních smluv napříč obchodními kanály* |
| Customer Service | [Aktivace Customer Service s Dynamics 365 Omnikanálem pro Customer Service](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | Prvotřídní zákaznická podpora je klíčem k poskytování personalizovaného a příjemného obchodního prostředí pro spotřebitele. V současné době existuje více obchodních kontaktních bodů, jako jsou fyzické obchody, online kanály a sociální kanály. Spotřebitelé očekávají personalizovanou podporu ve všech těchto kontaktních bodech. Tato funkce vám pomůže zvýšit konverze košíku na prodej, zvýšit personalizované zapojení se spotřebiteli a zlepšit služby zákazníkům díky integraci s Dynamics 365 Omnikanál pro Customer Service. | Povoleno správci/tvůrci |
| Elektronické obchodování | Podpora srovnávání produktů v e-shopu | Umožněte nakupujícím porovnávat produkty v široké škále kategorií, aby se sami mohli správně rozhodnout o nákupu. Tato funkce je k dispozici pro weby typu business-to-consumer (B2C) i B2B. | Konfigurátor webů | 
| Dárkové poukazy | Podpora tabulek maloobchodních dárkových karet pro sdílení dat mezi společnostmi | Dynamics headquarters podporuje možnost povolit sdílení dat mezi společnostmi pro konkrétní tabulky v architektuře Dynamics. V této funkci Dynamics 365 Commerce nově obsahuje podporu tabulek maloobchodních dárkových karet pro sdílení dat mezi společnostmi. Dárková karta v jedné společnosti tak nyní může mít svá data duplikována do jiné společnosti v prostředí. Změny provedené v původní tabulce firemních dárkových karet budou sdíleny se zduplikovanou tabulkou firemních dárkových karet. | Vývojáři |
| Výkon | Odebrání závislosti RTS pro scénáře „upravit zákazníka“ | Vysoká dostupnost a vysoký výkon jsou výchozí očekávání pro kanály v pokladním místě (POS) a elektronického obchodování. Aby bylo možné tato očekávání splnit, kanály Dynamics 365 Commerce se již nemusí spoléhat na komunikaci s Commerce headquarters v reálném čase, když jsou upravovány zákaznické informace. Schopnost asynchronně upravovat informace o zákaznících pro asynchronní a neasynchronní zákazníky může pomoci omezit volání v reálném čase do Commerce headquarters. | Povoleno správci/tvůrci |

## <a name="feature-state-changes-in-this-release"></a>Změny stavu funkcí v této verzi

V následující tabulce je uveden seznam funkcí, které jsou počínaje verze 10.0.29 povinné nebo ve výchozím nastavení zapnuté. Všechny tyto funkce se pro váš systém automaticky zapnou, jakmile provedete aktualizaci na verzi 10.0.29. Povinné funkce nelze vypnout, ale funkce, které jsou ve výchozím nastavení zapnuté, lze stále vypnout ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabulka také uvádí funkce, které byly dříve v Public Preview, ale změnily se tak, aby byly obecně dostupné ve verzi 10.0.29. Tato změna znamená, že funkce jsou nyní doporučeny pro použití v produkčních prostředích. Tyto funkce jsou ve výchozím nastavení vypnuté, pokud není uvedeno jinak. Pokud je chcete použít, musíte je výslovně povolit ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funkce | Titul | Nový stav funkce |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(Brazílie) Funkce aplikace Commerce specifické pro Brazílii | Zapnuto ve výchozím nastavení |
| RetailAdvancedGTETaxAdjustmentFeature | (Indie) Pro výkazy maloobchodu použít daň GST vypočtenou pro maloobchodní transakce v Retail POS | Zapnuto ve výchozím nastavení |
| RetailChronologicalInvoicePostingFeature_IT | (Itálie) Povolit maloobchodní faktury zaúčtované bez chronologického pořadí | Zapnuto ve výchozím nastavení |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (Mexiko) Úprava slev v globálním maloobchodním CFDI | Zapnuto ve výchozím nastavení |
| RetailFiscalIntegrationConfigurationEnhancementFeature | Přepsání technického profilu fiskální integrace | Zapnuto ve výchozím nastavení |
| RetailFiscalIntegrationConnectorLocationFeature | Přímá fiskální integrace z POS registrů | Zapnuto ve výchozím nastavení |
| RetailFiscalIntegrationLocalStorageBackupEnableFeature | Záloha místního úložiště fiskální integrace | Zapnuto ve výchozím nastavení |
| RetailFiscalIntegrationPostponeFiscalRegistrationFeature | Odložená registrace dokumentů | Zapnuto ve výchozím nastavení |
| RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | Stav fiskální registrace registrů POS | Zapnuto ve výchozím nastavení |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (Indie) Vypočítat daň GST na základě fakturační adresy pro objednávky elektronického obchodování | Zapnuto ve výchozím nastavení |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (Polsko) Výchozí stav prodejního dokladu pro maloobchodní faktury | Zapnuto ve výchozím nastavení |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (Mexiko) Zaokrouhlený přepočet pro částky základu daně v globálním Retail CFDI. | Zapnuto ve výchozím nastavení |
| RetailSupplementaryInvoiceFeature | Povolit doplňkové faktury za transakce cash and carry dokončené v maloobchodech | Zapnuto ve výchozím nastavení |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  Povolit rezervní zásoby a úrovně zásob    |  Zapnuto ve výchozím nastavení|
|RetailInboundOutboundInventoryValidationFeature|   Povolit ověření operace příchozích a odchozích zásob v POS   |   Zapnuto ve výchozím nastavení   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  Vylepšená logika výpočtu zásob na straně kanálu elektronického obchodování |   Zapnuto ve výchozím nastavení   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    Úpravy zásob v pokladním místě   |  Zapnuto ve výchozím nastavení  |
| RetailMultiplePickupDeliveryModeFeature |  Podpora více režimů vyzvednutí dodávky     |   Povinné    |
|  RetailProductAvailabilityOptimizationFeature |   Optimalizovaný výpočet dostupnosti produktu  |  Povinné |
|   RetailPricingDataManagerV2Feature   |   Zlepšit výkon cenového modulu Commerce |   Povinné |
|  RetailPricingPreventUnintendedRecalculationFeature   | Zabránění neúmyslnému výpočtu ceny u obchodních objednávek    |  Povinné  |
| RetailTeamsIntegration    |   Povolit integraci Microsoft Teams| Povinné   |  
| ConsumerEFDSyncProcessFeature_BR | (Brazílie) Synchronní zpracování NFC-e | Zapnuto ve výchozím nastavení |
| RetailFiscalIntegrationInternalAndExternalServicesEnableFeature | Podpora pro interní a externí konektory v rámci fiskální integrace | Povinné |
| RetailTaxRegistrationIdEnableFeature_BR | (Brazílie) Vyhledat zákazníky v Retail POS podle DIČ | Povinné |
| RetailTaxRegistrationIdEnableFeature_IN | (Indie) Vyhledat zákazníky v Retail POS podle DIČ | Povinné |
| RetailTaxRegistrationIdEnableFeature_IT | (Itálie) Správa informací o odběratelích v Retail POS | Povinné |
| RetailTaxRegistrationIdEnableFeature_PL | (Polsko) Správa informací o odběratelích v Retail POS | Povinné |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (Maloobchodní daň GST pro Indii) Aktualizovat dobropisy s odkazy na originální faktury | Povinné |
| RetailUserDefinedCertificateProfileFeature | Profily certifikátů definovaných uživatelem pro maloobchodní prodejny | Povinné |
  

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Microsoft Dynamics 365 Commerce 10.0.29 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.29 finančních a provozních aplikací (říjen 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). 

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.29, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2022

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si [Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2022](/dynamics365-release-plan/2022wave2/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-features"></a>Odstraněné a zastaralé funkce

Článek [Odstraněné nebo zastaralé funkce v Dynamics 365 Commerce](removed-deprecated-features-commerce.md) popisuje funkce, které byly pro Commerce odstraněny nebo jsou zastaralé.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v článku [Odebrané nebo zastaralé funkce v Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
