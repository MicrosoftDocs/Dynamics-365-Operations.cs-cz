---
title: Daně z online objednávek jsou nesprávně vypočítány
description: Tento článek poskytuje pokyny pro řešení potíží, které mohou pomoci, když jsou daně z online objednávek nesprávně vypočítány nebo když daňová skupina na prodejním řádku není správně nastavena.
author: Reza-Assadi
ms.date: 02/16/2022
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eefcfc983a7b3861caa4b4362d2813082b7963a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901614"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Daně z online objednávek jsou nesprávně vypočítány

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje pokyny pro řešení potíží, které mohou pomoci, když jsou daně z online objednávek nesprávně vypočítány nebo když daňová skupina na prodejním řádku není správně nastavena.

## <a name="description"></a>popis

Při zadání objednávky elektronického obchodu jsou daně nesprávně vypočítány nebo je nesprávně nastavena daňová skupina na prodejním řádku.

## <a name="resolution"></a>Řešení

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Konfigurace obecné skupiny DPH v centrále Commerce

Chcete-li nakonfigurovat obecné skupiny DPH v centrále Commerce, postupujte následovně.

1. Přejděte na **Daň \> Nepřímé daně \> DPH \> Skupina DPH**.
1. Na levém navigačním panelu vyberte daňovou skupinu, kterou chcete konfigurovat.
1. Na kartě s náhledem **Maloobchodní daň podle cíle** nakonfigurujte daně pro skupinu DPH.

> [!NOTE]
> U dopravy, která nezahrnuje DPH určenou podle adresy zákazníka, určuje daňovou skupinu dodací adresa řádku a daně podle cíle, které jsou nakonfigurovány pro daňovou skupinu. Další informace viz [Nastavení daní pro online obchody podle cílového místa](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Konfigurace DPH pro maloobchod v centrále Commerce

Chcete-li nakonfigurovat DPH pro maloobchod v centrále Commerce, postupujte následovně.

1. Přejděte na **Retail a Commerce \> Kanály \> Všechny obchody**.
1. Vyberte obchod, pro který chcete nakonfigurovat DPH.
1. Na kartě s náhledem **Všeobecné** v části **Prodejní daň** nakonfigurujte informace o DPH pro obchod.

> [!NOTE]
> U vyzvednutí produktu z obchodu daňová skupina pochází z obchodu, který je vybrán pro vyzvednutí. Další informace naleznete v tématu [Nastavení dalších daňových možností pro obchody](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Konfigurace DPH pro adresu zákazníka v centrále Commerce

Chcete-li nakonfigurovat DPH pro adresu zákazníka v centrále Commerce, postupujte následovně.

1. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.
1. Vyberte zákazníka, pro kterého chcete nakonfigurovat DPH.
1. Na kartě s náhledem **Adresy** vyberte adresu, pro kterou chcete konfigurovat DPH, vyberte **Další možnost** a potom vyberte **Pokročilé**.
1. Na kartě s náhledem **Obecné** vyberte **Daňová skupina**.
1. V poli **DPH** vyberte příslušnou hodnotu.

> [!NOTE]
> U dopravy, která zahrnuje DPH na adrese zákazníka, určuje doručovací adresa řádku daňovou skupinu pro řádek. Pokud zákazník odesílá na existující adresu, která má již nakonfigurovanou daňovou skupinu, bude použita stávající daňová skupina. Ve výchozím nastavení adresy nemají při vytvoření daňovou skupinu.

## <a name="additional-resources"></a>Další prostředky

[Konfigurace DPH pro online objednávky](../sales-tax-config.md)
