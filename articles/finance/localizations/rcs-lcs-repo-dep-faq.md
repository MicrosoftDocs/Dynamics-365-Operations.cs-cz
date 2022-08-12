---
title: Regulatory Configuration Service (RCS) - ukončení podpory úložiště Lifecycle Services (LCS)
description: Tento článek poskytuje informace o ukončení podpory úložiště Microsoft Dynamics Lifecycle Services (LCS), které je plánováno jako součást zavádění globálního úložiště Regulatory Configuration Service (RCS).
author: JaneA07
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: 65d45eaf618075e0c78881634fc77bda0fab277e
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065667"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – ukončení podpory úložiště Lifecycle Services (LCS)

[!include [banner](../includes/banner.md)]

Používání služby Microsoft Dynamics Lifecycle Services (LCS) jako úložiště pro konfigurace elektronického výkaznictví (ER) je označeno jako zastaralé. Toto rušení bude zahrnovat následující změny:

- Konfigurace vyrobené společností Microsoft, které se používají v aplikacích Microsoft Dynamics 365, již nebudou publikovány do knihovny sdíleného materiálu v LCS. Místo toho budou publikovány pouze prostřednictvím globálního úložiště RCS. Konfigurace pro Dynamics AX 2012 však budou nadále publikovány v knihovně sdíleného materiálu v LCS až do konce podpory životního cyklu AX 2012.
- Funkce, která vám umožní nahrát konfigurace do knihovny materiálů projektu v LCS z finančních a provozních aplikací a z RCS, bude deaktivována. Stále však budete moci použít prohlížeč v LCS k nahrání konfigurací do knihovny materiálů projektu. Proto budete i nadále moci přidávat konfigurace do LCS, aby je bylo možné zahrnout do balíčků řešení.
- Import konfigurací z LCS bude i nadále k dispozici a po nějakou dobu podporován ve finančních a provozních aplikacích a v RCS. Funkce však bude jednou ukončena. (Přesné datum ukončení podpory bude oznámeno později.)

## <a name="deprecation-notice"></a>Oznámení o ukončení podpory

Ukončení používání LCS jako úložiště bylo oznámeno v článku [Odebrané nebo zastaralé funkce v Dynamics 365 Finance – Oznámení o ukončení podpory LCS](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Plánované datum ukončení podpory je 1. dubna 2022.

## <a name="key-features"></a>Klíčové funkce

- Pomocí RCS můžete vytvářet a upravovat konfigurace ER a funkce globalizace.
- Přeneste konfigurace přímo z návrháře RCS do připojené aplikace, jako je např. prostředí Dynamics 365 Finance, abyste mohli rychle provádět a testovat změny ve svých konfiguracích.
- Centrálně ukládejte, sdílejte a spravujte životní cyklus konfigurací ER i funkcí globalizace prostřednictvím centralizovaného úložiště globálního úložiště.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Pokyny pro jednorázové a probíhající akce

Tato část popisuje sadu kroků, které je třeba provést jednou. Popisuje také kroky, které je poté nutné průběžně dokončovat.

### <a name="one-time-action"></a>Jednorázová akce

Importujte všechny požadované konfigurace z LCS do RCS a poté je publikujte z RCS do globálního úložiště. Pokud používáte knihovny materiálů specifických pro projekt k ukládání odvozených konfigurací v LCS, je nutné dokončit následující kroky, dokud je LCS stále přístupné.

1. Pokud instance RCS již není k dispozici, vytvořte ji. Další informace naleznete v tématu [Přehled RCS](rcs-overview.md).
2. Ve zřízené instanci RCS zaregistrujte pro každý projekt LCS v knihovně materiálů, která obsahuje odvozené konfigurace ER, příslušné úložiště LCS.
3. Importujte konfigurace ER z úložišť LCS do RCS. Další informace získáte v tématu [Import konfigurací z LCS](/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services).
4. Pokud není globální úložiště automaticky poskytováno, zaregistrujte jej v RCS.
5. Nahrajte všechny odvozené konfigurace z aktuální instance RCS do globálního úložiště. Použijte funkci **Konfigurační balíčky**, která vám pomůže s nahráváním. Další informace najdete v článku [Nahrávání do globálního úložiště RCS](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Do budoucna

Vizuální designéry v RCS používejte k následujícím účelům:

- Rozšiřte šablony poskytované společností Microsoft.
- Vytvořte nové konfigurace, které vaše organizace vyžaduje.
- Přizpůsobte funkce globalizace pro elektronickou fakturaci a službu výpočtu daní.

Úložiště globalizace používejte k následujícím účelům:

- Získejte přístup ke konfiguracím vytvořeným společností Microsoft a funkcím globalizace.
- Nahrajte konfigurace, které jste vytvořili nebo rozšířili, do globálního úložiště pro úložiště a sdílejte je v prostředí aplikací Dynamics 365 vaší organizace nebo s externími organizacemi. Další informace viz článek [Vytvoření konfigurací elektronického výkaznictví v RCS a jejich odeslání do globálního úložiště](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Znamená tato změna, že LCS nelze použít jako centrální úložiště pro konfigurace?

Ano. Funkce, která vám umožní nahrát konfigurace do knihovny materiálů projektu v LCS z finančních a provozních aplikací a z RCS, bude vyřazena. Stále však budete moci použít prohlížeč v LCS k nahrání konfigurací do knihovny materiálů projektu podle potřeby.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Myslel jsem, že RCS je náhradní úložiště pro import souborů globálních šablon. Nemyslel jsem si, že se používá k ukládání konfigurací. Co je správně?

RCS je designová služba pro vytváření a úpravy konfigurací ER. RCS má vlastní úložiště, které je známé jako globální úložiště. Toto úložiště se používá k ukládání konfigurací vytvořených v RCS. Až se LCS nebude používat jako úložiště, bude globální úložiště jediným zdrojem pro konfigurace Microsoftu. Chcete-li importovat všechny požadované konfigurace z LCS do RCS, musíte provést jednorázovou akci a poté je publikovat z RCS do globálního úložiště.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Jaký je navrhovaný způsob ukládání konfigurací bez LCS, aby bylo možné snadno spravovat a přenášet „testovací“ a „produkční“ konfigurace?

RCS používá koncept *připojené aplikace*. Připojená aplikace vytváří spojení mezi RCS a jakoukoli instancí finančních a provozních aplikací. Protože RCS lze použít k úpravám konfigurací, lze připojenou aplikaci použít k odeslání konfigurací přímo z návrháře do prostředí finančních a provozních aplikací. Proto můžete své konfigurace rychle změnit a otestovat, místo abyste museli procházet úložiště LCS na úrovni projektu.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Existují nějaké příklady, které ukazují nastavení a správu?

Žádné příklady nejsou, ale můžete provést dříve uvedené kroky v tomto článku a migrovat vaše konfigurace do globálního úložiště RCS.

### <a name="is-rcs-a-prerequisite-to-configure-electronic-reporting"></a>Je RCS nezbytným předpokladem pro konfiguraci elektronického hlášení?

Ano. RCS zahrnuje funkce, které podporují nastavení funkcí globalizace, které používají služby globalizace, jako je elektronická fakturace a služba výpočtu daní. Služba však má stejnou funkcionalitu vizuálního návrháře, která vám umožňuje rozšířit nebo vytvořit nové konfigurace ER. RCS také poskytuje správu životního cyklu pro konfigurace ER a funkce globalizace.

### <a name="which-regions-can-rcs-be-deployed-in"></a>Ve kterých regionech lze RCS nasadit?

RCS je k dispozici v následujících oblastech Azure:

- USA
- Indie
- Francie
- Evropa

Další informace o podpoře produktu viz [Přehled globalizačních služeb Dynamics](globalization-services-overview.md). Další informace o zeměpisné podpoře najdete v části [Dynamics 365 a Power Platform: Dostupnost, umístění dat, jazyk a lokalizace](https://aka.ms/rcs/D365Productavailabilityguide).

### <a name="whats-the-cost-of-using-rcs"></a>Jaké jsou náklady na používání RCS?

RCS a globalizační úložiště jsou poskytovány zdarma jako součást stávajících licencí finančních a provozních aplikací. S používáním služby návrhu RCS nebo ukládáním konfigurací v globálním úložišti nejsou spojeny žádné samostatné náklady. V současné době není omezen počet konfigurací ani připojených aplikací.
