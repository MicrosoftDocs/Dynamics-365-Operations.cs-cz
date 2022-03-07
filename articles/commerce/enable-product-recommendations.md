---
title: Povolit doporučení produktu
description: V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a7be82b3a40aba621693f080ff41767fdaea474
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466309"
---
# <a name="enable-product-recommendations"></a>Povolit doporučení produktu

[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce. Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Předběžná kontrola doporučení

1. Ujistěte se, že máte platnou licenci doporučení Dynamics 365 Commerce.
1. Zajistěte, aby byl obchod Entity připojen k účtu Azure Data Lake Storage Gen2 vlastněnému zákazníkem. Další informace naleznete v tématu [Ujistěte se, že Azure Data Lake Storage bylo zakoupeno a úspěšně ověřeno v prostředí](enable-ADLS-environment.md).
1. Potvrďte, že konfigurace identity Azure AD obsahuje záznam pro doporučení. Další informace o tom, jak provést tuto akci, je následující.
1. Zajistěte, aby bylo naplánováno každodenní obnovení Azure Data Lake Storage Gen2. Další informace naleznete v tématu [Zajistěte, aby aktualizace úložiště entity byla automatizovaná](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. Povolte měření RetailSale pro úložiště Entity. Další informace o tomto nastavení procesu naleznete v tématu [Práce s opatřeními](/dynamics365/ai/customer-insights/pm-measures).

Po dokončení výše uvedených kroků budete připraveni povolit doporučení.

## <a name="azure-ad-identity-configuration"></a>Konfigurace identity Azure AD

Tento krok je vyžadován pouze pro zákazníky, kteří provozují infrastrukturu jako konfiguraci služby (IaaS). Konfigurace identity Azure AD je pro zákazníky používající Azure Service Fabric automatická, ale doporučujeme ověřit, zda je nastavení nakonfigurováno podle očekávání.

### <a name="setup"></a>Nastavení

1. V centrále Commerce vyhledejte stránku **aplikací Azure Active Directory**.
1. Zkontrolujte, zda existuje položka pro **RecommendationSystemApplication-1**. Pokud záznam neexistuje, vytvořte jej pomocí následujících informací:

    - **ID klienta**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **Název**: RecommendationSystemApplication-1
    - **ID uživatele**: RetailServiceAccount

1. Uložit a zavřít stránku. 

## <a name="turn-on-recommendations"></a>Zapnutí doporučení

Chcete-li zapnout doporučení produktu, postupujte následujícím způsobem.

1. V centrále Commerce vyhledejte **Správa funkcí**.
1. Volbou **Vše** zobrazíte seznam dostupných funkcí. 
1. Do vyhledávacího pole zadejte **Doporučení**.
1. Vyberte funkci **Doporučení k produktu**.
1. V podokně vlastností **Doporučení produktů** vyberte **Ihned povolit**.

![Zapnutí doporučení.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - Výše uvedený postup spustí proces generování seznamů doporučení produktů. Mže trvat až několik hodin, než jsou seznamy k dispozici a lze je zobrazit na pokladním místě (POS) nebo v řešení Dynamics 365 Commerce.
> - Tato konfigurace nepovoluje všechny funkce doporučení. Pokročilé funkce, jako jsou přizpůsobená doporučení, „vzhled podobný obchodu“ a „popis podobný obchodu“, jsou ovládány vyhrazenými položkami správy funkcí. Informace o povolení těchto funkcí v centrále Commerce viz [Povolení přizpůsobených doporučení](personalized-recommendations.md), [Povolení doporučení „nakupovat podobný vzhled“](shop-similar-looks.md), a [Povolení doporučení „nakupovat podobný popis“](shop-similar-description.md).

## <a name="configure-recommendation-list-parameters"></a>Konfigurace parametrů seznamu doporučení

Ve výchozím nastavení poskytují seznamy doporučení produktů na bázi AI-ML navrhované hodnoty. Výchozí navrhované hodnoty lze změnit tak, aby vyhovovaly toku vašeho podniku. Další informace o tom, jak změnit výchozí parametry, naleznete v části [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).

## <a name="include-recommendations-in-e-commerce-experiences"></a>Zahrnout doporučení do prostředí elektronického obchodování

Po povolení doporučení v centrále Commerce jsou moduly Commerce používané k zobrazení výsledků doporučení pro prostředí elektronického obchodování připraveny ke konfiguraci. Další informace naleznete v tématu [Moduly kolekce produktu](product-collection-module-overview.md).

## <a name="show-recommendations-on-pos-devices"></a>Zobrazení doporučení na zařízeních POS

Po povolení doporučení v centrále Commerce je nutné přidat panel doporučení na řídicí obrazovku POS pomocí nástroje pro rozložení. Více o tomto procesu se dozvíte v části [Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS](add-recommendations-control-pos-screen.md). 

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
