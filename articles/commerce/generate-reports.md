---
title: Generování sestav online kanálu
description: V tomto tématu je popsán způsob generování sestav pro online kanál v Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ae7b73c7a51ffa606876072d607fc219f5f6a2ba
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410808"
---
# <a name="generate-online-channel-reports"></a>Generování sestav online kanálu


[!include [banner](includes/banner.md)]

V tomto tématu je popsán způsob generování sestav pro online kanál v Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

V Commerce můžete generovat a zobrazit několik sestav a sledovat tak, jak váš online kanál funguje.

## <a name="channel-summary-report"></a>Sestava souhrnu kanálu

V sestavě **Souhrn kanálů** je uveden souhrn následujících transakcí pro vybraný kanál:

- Prodejní transakce
- Platební transakce
- Daňové transakce
- Transakce slev

Chcete-li vygenerovat sestavu **Souhrn kanálů**, postupujte následujícím způsobem.

1. Přejděte na **Retail \> Retail a Commerce \> Prodejní sestavy \> Sestava souhrnu kanálu**.
1. Do pole **Od data** zadejte datum.
1. Do pole **Do data** zadejte datum.
1. V poli **Kanál** vyberte online kanál.
1. Vyberte **OK**.
 
## <a name="channel-sales-by-year-report"></a>Sestava kanálu prodeje podle roku 

Sestava **Sestava kanálu prodeje podle roku** zobrazuje srovnání ročního prodeje v rámci roku pro určitý obchod. Vyberte rok, ke kterému chcete porovnat prodej, a sestava porovná prodej za vybraný rok s prodejem za předchozí rok.

Chcete-li vygenerovat sestavu **Sestava kanálu prodeje podle roku**, postupujte následujícím způsobem.

1. Přejděte na **Retail \> Retail a Commerce \> Prodejní sestavy \> Sestava kanálu prodeje podle roku**.
1. Zadejte rok do pole **Z kalendářního roku**.
1. Zadejte rok do pole **Do kalendářního roku**.
1. V poli **Kanál** vyberte online kanál.
1. Vyberte **OK**.

## <a name="channel-sales-by-hour-report"></a>Sestava prodejního kanálu podle hodin

Sestava **Prodejní kanál podle hodin** zobrazuje metriku prodeje za hodinu pro vybraný kanál nebo provozní jednotku.

Chcete-li vygenerovat sestavu **Prodejní kanál podle hodin**, postupujte následujícím způsobem.

1. Přejděte na **Retail \> Retail a Commerce \> Prodejní sestavy \> Sestava kanálu prodeje podle hodiny**.
1. Do pole **Od data** zadejte datum.
1. Do pole **Do data** zadejte datum.
1. V poli **Kanál** vyberte online kanál.
1. Vyberte **OK**.

## <a name="top-customers-report"></a>Sestava nejlepších odběratelů

Sestava **Přední odběratelé** zobrazuje prodejní metriky nejlepších *N* odběratelů pro vybraný kanál nebo provozní jednotku. Hodnota *N* je číslo od 10 do 100 a je založena na agregované míře vybrané uživatelem.

Chcete-li vygenerovat sestavu **Přední odběratelé**, postupujte následujícím způsobem.

1. Přejděte na **Retail \> Retail a Commerce \> Prodejní sestavy \> Sestava nejlepších odběratelů**.
1. Do pole **Od data** zadejte datum.
1. Do pole **Do data** zadejte datum.
1. V poli **Kanál** vyberte online kanál.
1. Vyberte **OK**.

## <a name="top-discounts-report"></a>Sestava největších slev

Sestava **Největší slevy** zobrazuje prodejní metriky nejlepších *N* slev pro vybraný kanál nebo provozní jednotku. Hodnota *N* je číslo od 10 do 100 a je založena na agregované míře vybrané uživatelem.

Chcete-li vygenerovat sestavu **Největší slevy**, postupujte následujícím způsobem.

1. Přejděte na **Retail \> Retail a Commerce \> Prodejní sestavy \> Sestava největších slev**.
1. Do pole **Od data** zadejte datum.
1. Do pole **Do data** zadejte datum.
1. V poli **Kanál** vyberte online kanál.
1. Vyberte **OK**.

## <a name="top-products-report"></a>Sestava nejlepších produktů

Sestava **Nejlepší produkty** zobrazuje prodejní metriky nejlepších *N* produktů pro vybraný kanál nebo provozní jednotku. Hodnota *N* je číslo od 10 do 100 a je založena na agregované míře vybrané uživatelem.

Chcete-li vygenerovat sestavu **Nejlepší produkt**, postupujte následujícím způsobem.

1. Přejděte na **Retail \> Retail a Commerce \> Prodejní sestavy \> Sestava nejlepších produktů**.
1. Do pole **Od data** zadejte datum.
1. Do pole **Do data** zadejte datum.
1. V poli **Kanál** vyberte online kanál.
1. Vyberte **OK**.

## <a name="category-sales-report"></a>Prodejní sestava kategorií

Sestava **Prodejní kategorie** zobrazuje metriky prodeje za vybrané období pro každý uzel hierarchie kategorií pro vybraný kanál nebo provozní jednotku.

Chcete-li vygenerovat sestavu **Prodejní kategorie**, postupujte následujícím způsobem.

1. Přejděte na **Retail a Commerce \> Dotazy a sestavy \> Prodejní sestavy \> Prodejní sestava kategorií**.
1. Do pole **Od data** zadejte datum.
1. Do pole **Do data** zadejte datum.
1. V poli **Kanál** vyberte online kanál.
1. Vyberte **OK**.

## <a name="organization-sales-report"></a>Sestava prodejů organizace

Sestava **Prodeje organizace** zobrazuje výkonnost vašich obchodů podle organizační jednotky. Tato sestava zahrnuje prodejní množství a částku podle obchodu a ziskovou marži pro každý obchod. Organizační jednotka je založena na výchozí hierarchii sestav.

Chcete-li vygenerovat sestavu **Prodeje organizace**, postupujte následujícím způsobem.

1. Přejděte na **Retail a Commerce \> Dotazy a sestavy \> Prodejní sestavy \> Sestava prodejů organizace**.
1. Do pole **Od data** zadejte datum.
1. Do pole **Do data** zadejte datum.
1. Vyberte **OK**.

## <a name="additional-resources"></a>Další zdroje

- [Domovská stránka aplikace Commerce](../retail/index.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]