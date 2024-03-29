---
title: Regulatory Configuration Service
description: Tento článek poskytuje přehled schopností Regulatory Configuration Service (RCS) a vysvětluje, jak ke službě přistupovat.
author: kfend
ms.date: 06/04/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
ms.openlocfilehash: c04b13ef05424b27b5abcc2ac7490a7b75797bf5
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713910"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) je samostatná služba návrhu a správy životního cyklu pro funkce globalizace bez kódování / s malým množstvím kódování. RCS umožňuje zúčastněným stranám globalizace rozšířit a přizpůsobit klíčové oblasti globalizace v oblasti daní, elektronické fakturace, regulačních zpráv, bankovnictví a obchodních dokumentů, aniž by bylo nutné zapojovat vývojáře. Tento globalizační přístup bez kódování / s malým množstvím kódování umožňuje globalizaci snazší, rychlejší a nákladově efektivnější při vytváření nebo rozšiřování.

RCS poskytuje následující možnosti:

- Podpora všech funkcí, které poskytuje elektronické výkaznictví (ER).
- Předpoklad ke konfiguraci nových globálních mikroslužeb.
- Podpora elektronické fakturace. Další informace získáte v tématu [Elektronická fakturace](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Podporuje výpočet daně. Další informace naleznete v tématu [Daňová služba](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Podpora nových funkcí globalizačních funkcí, která zjednodušuje správu životního cyklu vícekomponentních funkcí a poskytuje další možnosti konfigurace akcí a nastavení parametrů funkcí. Další informace viz [Regulatory Configuration Service – zjednodušená správa funkcí globalizace pro globalizační služby](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Podpora centralizovaného publikování, ukládání a sdílení vlastních konfigurací v globálním úložišti pro zjednodušení správy konfigurace bez nutnosti použití Microsoft Dynamics Lifecycle Services (LCS).

## <a name="access-rcs"></a>Přístup k RCS

Můžete se zaregistrovat nebo přihlásit do RCS ze [stránky Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

![Registrace/přihlášení k RCS.](media/202103_RCS%20Marketing%20page_updated_1.jpg)

Na stránce **Regulatory Configuration Service** zkontrolujte a přijměte doplňkové podmínky pro používání služby a poté vyberte jedno z následujících tlačítek:

- **Zaregistrovat se**, pokud službu používáte poprvé a používáte pracovní e-mailovou adresu k zajištění prostředí služby vaší organizaci
- **Přihlásit se**, pokud jste se již do služby zaregistrovali a chcete přistupovat k prostředí vaší organizace

> [!NOTE] 
> Jakmile se zaregistrujete, doporučujeme přidat do prostředí RCS dalšího uživatele SysAdmin. Tento uživatel bude zřízen jako spolusprávce pro prostředí. To pomůže zajistit stabilitu pro přístup k prostředí RCS, protože rolí SysAdmin je správa uživatelů pro toto prostředí. Uživatelé můžete přidávat pomocí **Pracovní prostor RCS > Správa systému**.

## <a name="regional-availability"></a>Regionální dostupnost

RCS je obecně k dispozici v následujících oblastech:

- Spojené státy americké
- Indie
- Francie
- Evropa

Úplný seznam oblastí najdete v části [Dynamics 365 a Power Platform: Dostupnost, umístění dat, jazyk a lokalizace](https://aka.ms/dynamics_365_international_availability_deck).

> [!NOTE] 
> RCS není aktuálně k dispozici pro Government Community Cloud (GCC).

## <a name="rcs-default-company"></a>Výchozí společnost RCS

Funkce doby návrhu, která se používá v RCS, je sdílena všemi společnostmi. Neexistuje žádná funkce specifická pro jednu společnost. Proto doporučujeme ve vašem prostředí RCS použít jednu společnost **DAT**.

V některých scénářích však možná budete chtít, aby formáty ER používaly parametry, které souvisejí s konkrétním právním subjektem. Pouze v těchto scénářích byste měli použít výchozí přepínač společnosti. Ukázku najdete v tématu [Konfigurace formátů elektronického výkaznictví pro použití parametrů zadaných pro právnickou osobu](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).

## <a name="related-rcs-documentation"></a>Související dokumentace RCS

Další informace o souvisejících součástech naleznete v následujících tématech:

- **RCS:**

    - [Vytvoření konfigurací elektronického výkaznictví v RCS a jejich odeslání do globálního úložiště](rcs-global-repo-upload.md)

- **Globální úložiště:**

    - [Vytvoření konfigurace ER a nahrání do globálního úložiště](rcs-global-repo-upload.md)
    - [Sdílení konfigurace v globálním úložišti](rcs-global-repo-share-configuration.md)
    - [Rozšířené filtrování v globálním úložišti](enhanced-filtering-global-repo.md)
    - [Stažení konfigurací elektronického výkaznictví z globálního úložiště](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Ukončení konfigurací v globálním úložišti](discontinuing-configurations-rcs-global-repo.md)
    - [Regulatory Configuration Service (RCS) – ukončení podpory úložiště Lifecycle Services (LCS)](rcs-lcs-repo-dep-faq.md)

- **Globalizační funkce:**

    - [Regulatory Configuration Service (RCS) – Globalizační funkce](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>Řešení potíží s přihlášením do RCS

Při registraci do RCS ze stránky služby se můžete setkat s problémem, který souvisí se službou Azure Active Directory (Azure AD). Chybová zpráva, která se zobrazí, naznačuje, že registrace do RCS je aktuálně vypnutá a je nutné ji zapnout, abyste mohli dokončit proces registrace.

![Chybová zpráva registrace RCS.](media/01_RCSSignUpError.jpg)

K problému dochází, protože nemáte povoleno přihlášení k odběru ad hoc předplatných a ve vašem klientu musí být zapnuta vlastnost `AllowAdHocSubscriptions`. 

- Pokud vaše IT oddělení spravuje klienty Azure vaší organizace, kontaktujte toto oddělení a nahlaste problém.
- Pokud jste zodpovědní za správu svých klientů Azure, můžete problémy vyřešit podle pokynů v článku [K čemu je samoobslužná registrace Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).
