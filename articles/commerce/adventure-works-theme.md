---
title: Přehled motivu Adventure Works
description: Tento článek poskytuje přehled motivu Adventure Works a popisuje, jak ho použít na stránky webu v Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: ae2af73a17e03ca216665e515ac4739e02944b8c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278671"
---
# <a name="adventure-works-theme-overview"></a>Přehled motivu Adventure Works

[!include [banner](includes/banner.md)]

Tento článek poskytuje přehled motivu Adventure Works a popisuje, jak ho použít na stránky webu v Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce má motiv pro elektronický obchod s názvem Adventure Works. Motiv Adventure Works představuje sportovní a rekreační produkty a je optimalizováno pro bohatý a vylepšený zážitek z vyprávění. Poskytuje moderní vzhled, nové rozvržení a animační efekty, které zákazníkům v oblasti elektronického obchodování nabízejí pohlcující a poutavý zážitek z online nakupování.

## <a name="trial-environments-in-commerce"></a>Zkušební prostředí v Commerce

Chcete-li zjistit, jak vypadá motiv Adventure Works, když je nasazen pro weby business-to-consumer (B2C) a business-to-business (B2B), navštivte následující zkušební weby:

- [Web B2C Adventure Works](https://www.adventure-works.com/)
- [Web B2B Adventure Works](https://www.adventure-works.com/business)

## <a name="theme-capabilities"></a>Možnosti motivu

Motiv Adventure Works poskytuje následující nové možnosti:

- Modul přehrávače videa nyní podporuje funkci nadpisu, odstavce a odkazů pro další vyprávění.
- Existují lepší přechody obsahu prostřednictvím animace.
- Akce "přidání do košíku" vyvolá minikošík místo oznámení.
- Modul rychlého zobrazení je podokno, které se zasouvá do výřezů na stolních i mobilních zařízeních.
- Pro stránky webu existují nová rozvržení. 
- Marketingový obsah lze nakonfigurovat pro košík a mini košík, když jsou prázdné.
- Mini košík může zobrazovat propagační zprávy, například „Doprava zdarma u objednávek nad 50 USD.“
- Karty popisu se vykreslují na stránkách vyhledávání a kategorií.

Motiv Adventure Works nyní obsahuje následující vyprávěcí moduly v knihovně modulů Commerce:

- [Modul seznamu dlaždic](tile-list-module.md)
- [Interaktivní modul funkcí](interactive-feature-module.md)
- [Aktivní modul obrázků](active-image-module.md)
- [Modul odběru](subscribe-module.md)
- [Modul seznamu obrázků](image-list-module.md)

Motiv Adventure Works plně reaguje a poskytuje optimalizované prostředí pro zobrazení pro stolní počítače, mobilní zařízení a tablety.

> [!IMPORTANT]
> Motiv Adventure Works a nové moduly jsou k dispozici od Dynamics 365 Commerce verze 10.0.20.

Následující obrázek ukazuje příklad domovské stránky, která používá motiv Adventure Works.

![Příklad domovské stránky, která používá motiv Adventure Works](./media/aw_b2c.PNG)

Následující obrázek ukazuje příklad stránky seznamu, která používá motiv Adventure Works.

![Příklad stránky seznamu, která používá motiv Adventure Works](./media/Aw_list.PNG)

Následující obrázek ukazuje příklad stránky s podrobnostmi o produktu (PDP), která používá motiv Adventure Works.

![Příklad stránky s podrobnostmi o produktu (PDP), která používá motiv Adventure Works](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>Použití Adventure Works pro weby B2B

Motiv Adventure Works je také referenčním motivem pro weby mezi podniky (B2B). Všechny B2B moduly a pracovní toky jsou představeny v motivu Adventure Works. Informace o nastavení webu B2B najdete v části [Nastavení webu B2B](./b2b/set-up-b2b-site.md).

Následující obrázek ukazuje příklad domovské stránky B2B, která používá motiv Adventure Works.

![Příklad domovské stránky B2B, která používá motiv Adventure Works](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>Rozšíření motivu

Motiv Adventure Works obsahuje několik rozšíření motivů, například rozšíření **Zobrazit rozšíření** a **Definice modulu**. Motiv Adventure Works lze použít jako referenční motiv k vytvoření podobných rozšíření. Například stránka seznamu v motivu Adventure Works je implementována jako rozšíření zobrazení, které má horizontální panel zpřesnění. (Naproti tomu v motivu Fabrikam se používá zpřesňující modul levého podokna.)

Stejně tak ostatní moduly obsahují rozšíření definice modulů. Například [modul ikony vozíku](cart-icon-module.md) obsahuje dva další sloty **Prázdný vozík** a **Propagační obsah**, které jsou implementovány pomocí rozšíření definice modulu. Navíc nová vlastnost **Mobilní logo** byla přidána vlastnost do modulu záhlaví pro podporu loga v mobilních zobrazeních. Tato vlastnost je implementována jako rozšíření definice záhlaví modulu.

Další informace o rozšířeních motivů najdete v části [Rozšíření motivu](e-commerce-extensibility/theme-module-extensions.md).

## <a name="install-the-adventure-works-theme"></a>Instalace motivu Adventure Works

Informace o tom, jak nainstalovat motiv Adventure Works, najdete v části [Nainstalujte si motiv Adventure Works ](install-adventure-works.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul seznamu dlaždic](tile-list-module.md)

[Modulu interaktivní funkce](interactive-feature-module.md)

[Modul aktivního obrázku](active-image-module.md)

[Modulu přihlášení k odběru](subscribe-module.md)

[Modul seznamu obrázků](image-list-module.md)

[Rozšíření motivu](e-commerce-extensibility/theme-module-extensions.md)

[Modul ikony košíku](cart-icon-module.md)

[Vytvoření webu elektronického obchodu B2B](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
