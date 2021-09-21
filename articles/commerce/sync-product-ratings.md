---
title: Synchronizace hodnocení produktů v Dynamics 365 Commerce
description: Toto téma popisuje, jak synchronizovat hodnocení produktu v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a50c09dc9fd8a4c18bbd01c70338279ac0ad9ae6
ms.sourcegitcommit: 81bc42551e6c9af6ad38908afb606ee1f8d3c44b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473518"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>Synchronizace hodnocení produktů v Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak synchronizovat hodnocení produktu v Microsoft Dynamics 365 Commerce.

Chcete-li využívat hodnocení produktů v omnikanálech, jako je například na pokladním místě (POS) a v kontaktních střediscích, musí být hodnocení produktů ze služby hodnocení a recenzí importována do databáze velkoobchodní sítě. Pokud jsou hodnocení produktů k dispozici v omnikanálech, mohou zákazníkům pomoci při jejich interakci s prodejcem.

Toto téma popisuje následující úkoly:

1. Nakonfigurujte **úlohu synchronizace hodnocení produktu** jako dávkovou úlohu a synchronizujte hodnocení produktu ze **služby hodnocení a recenzí**.
1. Ověřte, že dávková úloha synchronizace hodnocení produktu proběhla úspěšně.
1. Zajistěte dostupnost hodnocení produktu na POS.

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>Konfigurace maloobchodní dávkové úlohy k synchronizaci hodnocení produktu

> [!IMPORTANT]
> Dříve než začnete, zkontrolujte, zda je nainstalována verze Dynamics 365 Commerce 10.0.6 nebo vyšší.

### <a name="initialize-the-commerce-scheduler"></a>Inicializujte velkoobchodní plánovač

Pro inicializaci velkoobchodního plánovače postupujte takto.

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Inicializovat plánovač velkoobchodu**. Případně vyhledejte "inicializovat velkoobchodní plánovač".
1. V dialogovém okně **Inicializovat velkoobchodní plánovač** zkontrolujte, zda je možnost **Odstranit existující konfiguraci** nastavena na hodnotu **Ne**, a pak vyberte **OK**.

### <a name="verify-the-retailproductrating-subjob"></a>Ověřit dílčí úlohu RetailProductRating

Chcete-li ověřit, zda existuje dílčí úloha **RetailProductRating**, postupujte podle následujících kroků.

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Dílčí úlohy plánovače**. Případně vyhledejte "Plánovač dílčích úloh".
1. V seznamu dílčích úloh vyhledejte nebo vyhledejte dílčí úlohu **RetailProductRating**.

Následující ilustrace znázorňuje příklad stránky odrobnosti dílčích úloh v Commerce.

![Podrobnosti o dílčí úloze RetailProductRating.](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Pokud nenajdete dílčí úlohu **RetailProductRating**, je možné, že jste již před inicializací velkoobchodního plánovače spustili úlohu **Synchronizace hodnocení produktů** a **1040 CDX**. V takovém případě spusťte úlohu **Úplná synchronizace dat** provedením následujících kroků.

> 1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Databáze kanálu**. Případně můžete vyhledat "Databáze kanálů".
> 1. Vyberte databázi kanálů, která má být synchronizována.
> 1. V podokně akcí vyberte **Úplná synchronizace dat**.
> 1. V rozevíracím dialogovém okně **Vybrat plán distribuce** vyberte **1040 - produkty** a poté vyberte **OK**.
> 1. Zopakováním kroků předchozího postupu ověřte, zda byla vytvořena dílčí úloha **RetailProductRating**.

### <a name="import-product-ratings"></a>Import hodnocení produktů

Chcete-li importovat hodnocení produktů do velkoobchodu ze služby hodnocení a recenze, postupujte podle následujících kroků.

1. Přejděte na **Retail and Commerce \> Nastavení centrály \> Velkoobchodní plánovač \> Úloha synchronizace hodnocení produktů**. Případně vyhledejte "Úloha synchronizace hodnocení produktů".
1. V dialogovém okně **Hodnocení vyžádaných produktů** na pevné záložce **Spustit na pozadí** vyberte **Opakování**.
1. V dialogovém okně **Definovat opakování** nastavte způsob opakování. (Doporučená hodnota je dvě hodiny.) Neplánujte opakování, které je menší než jedna hodina.
1. Vyberte **OK**.
1. Nastavte **Dávkové zpracování** na **Ano**. Toto nastavení pomáhá zaručit, že budete moci auditovat protokoly a ověřit stav spuštění dávkové úlohy.
1. Výběrem **OK** naplánujte dávkovou úlohu.

Následující ilustrace znázorňuje příklad konfigurace dílčích úloh v Commerce.

![Konfigurace dávkové úlohy hodnocení produktů pro synchronizaci.](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Ověřte, že dávková úloha synchronizace hodnocení produktu proběhla úspěšně

Chcete-li ověřit, zda byla dávková úloha **Synchronizace hodnocení produktů** úspěšná, postupujte následujícím způsobem.

1. Přejděte na **Retail and Commerce \> Správce systému \> Dotazy \> Dávkové úlohy** nebo, pokud používáte skladovou jednotku (SKU) pouze pro Commerce, **Retail and Commerce \> Dotazy a sestavy \> Dávkové úlohy**. Případně vyhledejte "Dávkové úlohy."
1. Chcete-li zobrazit podrobné informace o dávkové úloze, v seznamu dávkové úlohy ve sloupci **Popis úlohy** vyhledejte popis, který obsahuje "Hodnocení vyžádaného produktu."
1. Vyberte ID úlohy pro zobrazení podrobností dávkové úlohy, jako je například plánované datum a čas zahájení a text opakování.

Na následujícím obrázku je znázorněn příklad podrobností dávkové úlohy v Commerce, když je dávková úloha naplánována na spuštění v intervalech dvou hodin.

![Podrobnosti dávkové úlohy Synchronizace hodnocení produktů.](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Zajistěte dostupnost hodnocení produktu na POS

Řešení pro hodnocení a recenze v Dynamics 365 Commerce je omnikanálové řešení. Hodnocení produktů však není ve výchozím nastavení v POS zobrazeno. Chcete-li zákazníkům pomoci v obchodech vidět hodnocení a recenze, pokud jim pomáhají pracovníci obchodu, musíte hodnocení produktů zapnout v POS.

Chcete-li zapnout hodnocení produktů v POS, postupujte podle následujících kroků.

1. Přejděte na možnost **Retail a Commerce \> Nastavení velkoobchodu \> Parametry \> Parametry velkoobchodu**. Případně můžete vyhledat "Parametry velkoobchodu".
1. Na kartě **Konfigurační parametry** vyberte možnost **Nový**.
1. Zadejte název, například **RatingsAndReviews.EnableProductRatingsForRetailStores**, a nastavte hodnotu na **true**.
1. Zvolte **Uložit**.
1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**. Případně můžete vyhledat hodnotu "Plán distribuce".
1. V seznamu úloh vyberte **1110** (**Globální konfigurace**) a pak vyberte možnost **Spustit nyní.**
1. Po úspěšném spuštění úlohy ověřte, zda jsou nyní v POS zobrazena hodnocení produktů.

Na následujícím obrázku je znázorněn příklad konfigurace parametrů velkoobchodu, které zapínají hodnocení produktů na POS.

![Konfigurace parametrů velkoobchodu pro hodnocení produktů v POS.](media/rnr-hq-enable-ratings-in-pos.png)

Následující obrázek znázorňuje příklad hodnocení produktů na POS.

![Hodnocení produktů na POS.](media/rnr-pos-catalog-ratings.png)

Následující obrázek znázorňuje příklad hodnocení produktů v kanálech kontaktního střediska.

![Hodnocení produktu v kanálu kontaktního střediska.](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled hodnocení a recenzí](ratings-reviews-overview.md)

[Připojení k používání hodnocení a recenzí](opt-in-ratings-reviews.md)

[Správa hodnocení a recenzí](manage-reviews.md)

[Konfigurace hodnocení a recenzí](configure-ratings-reviews.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
