---
title: Povolit ruční publikování hodnocení a recenzí moderátorem
description: Tento článek popisuje, jak povolit ruční publikování hodnocení a recenzí moderátorem v Microsoft Dynamics 365 Commerce a jak ručně publikovat hodnocení a recenze.
author: gvrmohanreddy
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
manager: annbe
ms.openlocfilehash: 6591e18ff8e83ec9030d91d8348271b8113e453f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276768"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>Povolit ruční publikování hodnocení a recenzí moderátorem

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak povolit ruční publikování hodnocení a recenzí moderátorem v Microsoft Dynamics 365 Commerce a jak ručně publikovat hodnocení a recenze.

Dynamics 365 Commerce pro hodnocení a recenze používá Azure Cognitive Services k automatickému sepsání vulgárních výrazů v názvech a obsahu recenzí a k publikování hodnocení a recenzí. Při kontrole a publikování hodnocení a recenzí na vašem webu elektronického obchodu tedy není vyžadován ruční zásah.

Některé podniky však mohou upřednostňovat, aby moderátoři recenze před jejich zveřejněním ručně zkontrolovali a schválili. Chcete -li povolit ruční publikování hodnocení a recenzí moderátorem, musíte povolit funkci **Vyžadovat moderátora pro hodnocení a recenze** v tvůrci webu Commerce.

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>V tvůrci webu obchodu povolte funkci Vyžadovat moderátora pro hodnocení a recenze

Pokud chcete povolit funkci **Vyžadovat moderátora pro hodnocení a recenze** v tvůrci webu obchodu, postupujte následovně.

1. Přejděte na **Domů \> Recenze \> Nastavení**.
1. Nastavte možnost **Vyžadovat moderátora pro hodnocení a recenze** na **Zapnuto**.

> [!NOTE]
> Povolením funkce **Vyžadovat moderátora pro hodnocení a recenze** zastavíte automatické publikování hodnocení a recenzí, takže ruční publikování je nyní vyžadováno. Azure Cognitive Services však budou i nadále redigovat vulgární výrazy v názvech recenzí a obsahu.

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>Publikování hodnocení a recenzí

Když povolíte funkci **Vyžadovat moderátora pro hodnocení a recenze**, musí moderátor ručně zkontrolovat a publikovat hodnocení a recenze, aby se zobrazovaly na vašem webu elektronického obchodování.

Chcete-li si zkontrolovat a publikovat hodnocení a recenze v tvůrci webu v Commerce, postupujte následujícím způsobem.

1. Přejděte na **Recenze \> Moderování**.
1. Pokud pole **Stav** pro řádek je nastaveno na **Nepublikovaný**, hodnocení a recenze v tomto řádku ještě nebyly zveřejněny. Chcete -li zobrazit pouze nepublikovaná hodnocení a recenze, vyberte **Stav: Vyžaduje kontrolu** ve stavovém filtru nad mřížkou.
1. Vyberte jedno nebo více hodnocení a recenzí, jejichž stav je **Nepublikovaný** a poté vyberte **Publikovat** na příkazovém řádku. Vybraná hodnocení a recenze se přidají do fronty publikování a po publikování se objeví na webu elektronického obchodování.

> [!NOTE]
> - Po zveřejnění hodnocení a recenze se hodnota stavu změní z **Nepublikovaný** na hodnotu null (prázdné pole).
> - Pokud vyberete více hodnocení a recenzí, které mají smíšené stavy, a poté vyberete **Publikovat**, budou publikovány hodnocení a recenze, které dosud nebyly publikovány. Hodnocení a recenze, které již byly publikovány, však znovu publikovány nebudou.

Následující ilustrace ukazuje příklad, kde jsou na stránce **Moderování** v nástroji Commerce site builder vybrána nepublikovaná hodnocení a recenze.

![Tři nepublikovaná hodnocení a recenze vybrané na stránce Moderování v nástroji Commerce site Builder.](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>Další prostředky

[Přehled hodnocení a recenzí](ratings-reviews-overview.md)

[Připojení k používání hodnocení a recenzí](opt-in-ratings-reviews.md)

[Správa hodnocení a recenzí](manage-reviews.md)

[Konfigurace hodnocení a recenzí](configure-ratings-reviews.md)

[Synchronizace hodnocení produktů](sync-product-ratings.md)

[Import a export hodnocení a recenzí](import-export-reviews.md)

[Konfigurace ověřování mezi službami](service-to-service-auth.md)

[Nejčastější dotazy k hodnocení a recenzím](ratings-reviews-faq.md)
