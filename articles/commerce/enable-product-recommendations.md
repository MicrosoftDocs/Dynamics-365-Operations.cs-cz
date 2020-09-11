---
title: Povolit doporučení produktu
description: V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b201e5481cfaf5bb6cd64a89cdb6b5a91f31447f
ms.sourcegitcommit: d3b970c3b93d8be12886b1c5a6bf91f0b33726dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/19/2020
ms.locfileid: "3700835"
---
# <a name="enable-product-recommendations"></a>Povolit doporučení produktu

[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce. Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Předběžná kontrola doporučení

Před povolením berte na vědomí, že doporučení produktů jsou podporována pouze u zákazníků Commerce, kteří migrovali své úložiště pomocí Azure Data Lake Storage. 

Před povolením doporučení musí být v administravě povoleny následující konfigurace:

1. Ujistěte se, že Azure Data Lake Storage bylo zakoupeno a úspěšně ověřeno v prostředí. Další informace naleznete v tématu [Ujistěte se, že Azure Data Lake Storage bylo zakoupeno a úspěšně ověřeno v prostředí](enable-ADLS-environment.md).
2. Zkontrolujte, zda byla aktualizace úložiště entity automatizovaná. Další informace naleznete v tématu [Zajistěte, aby aktualizace úložiště entity byla automatizovaná](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. Potvrďte, že konfigurace identity Azure AD obsahuje záznam pro doporučení. Další informace o tom, jak provést tuto akci, je následující.

Dále zkontrolujte, zda byly povoleny ukazatele RetailSale. Další informace o tomto nastavení procesu naleznete v tématu [Práce s opatřeními](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="azure-ad-identity-configuration"></a>Konfigurace identity Azure AD

Tento krok je vyžadován pro všechny zákazníky, kteří provozují infrastrukturu jako konfiguraci služby (IaaS). U zákazníků, kteří provozují prostředky v rámci služby (SF), by tento krok měl být automaticky a doporučujeme ověřit, zda je nastavení nakonfigurováno očekávaným způsobem.

### <a name="setup"></a>Nastavení

1. V administrativě vyhledejte stránku **Aplikace Azure Active Directory**.
2. Ověřte, zda existuje položka pro "RecommendationSystemApplication-1".

Pokud položka neexistuje, přidejte novou položku s následujícími informacemi:

- **ID klienta** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **Název** -RecommendationSystemApplication-1
- **ID uživatele** – RetailServiceAccount

Uložit a zavřít stránku. 

## <a name="turn-on-recommendations"></a>Zapnutí doporučení

Chcete-li zapnout doporučení produktu, postupujte následujícím způsobem.

1. V centrále Commerce vyhledejte **Správa funkcí**.
1. Volbou **Vše** zobrazíte seznam dostupných funkcí. 
1. Do vyhledávacího pole zadejte **Doporučení**.
1. Vyberte funkci **Doporučení k produktu**.
1. V podokně vlastností **Doporučení produktů** vyberte **Ihned povolit**.

![Zapnutí doporučení](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> Tento postup spustí proces generování seznamů doporučení produktů. Mže trvat až několik hodin, než jsou seznamy k dispozici a lze je zobrazit na pokladním místě (POS) nebo v řešení Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>Konfigurace parametrů seznamu doporučení

Ve výchozím nastavení poskytují seznamy doporučení produktů na bázi AI-ML navrhované hodnoty. Výchozí navrhované hodnoty lze změnit tak, aby vyhovovaly toku vašeho podniku. Další informace o tom, jak změnit výchozí parametry, naleznete v části [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Zobrazení doporučení na zařízeních POS

Po povolení doporučení v administrativě Commerce je nutné přidat panel doporučení na řídicí obrazovku POS pomocí nástroje pro rozložení. Více o tomto procesu se dozvíte v části [Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Povolení přizpůsobených doporučení

V aplikaci Dynamics 365 Commerce mohou maloobchodní prodejci vytvářet přizpůsobená doporučení k produktu (označované také jako individuální nastavení). Tímto způsobem lze přičlenit individuální doporučení do online prostředí zákazníků a na pokladním místě. Je-li funkce přizpůsobení zapnuta, může systém přidružit nákup a informace o produktu uživatele ke generování doporučení pro jednotlivé produkty.

Další informace o přizpůsobených doporučení získáte v tématu [Povolení přizpůsobených doporučení](personalized-recommendations.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Povolit doporučení typu „podobný vzhled“](shop-similar-looks.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Přidat doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakce](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)

