---
title: Generování sestav online kanálu
description: V tomto článku je popsán způsob generování sestav pro online kanál v Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 0523e74d2bfb4191e467edc001daf9178c7b4bf6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268309"
---
# <a name="generate-online-channel-reports"></a>Generování sestav online kanálu

[!include [banner](includes/banner.md)]

V tomto článku je popsán způsob generování sestav pro online kanál v Microsoft Dynamics 365 Commerce.

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

- [Domovská stránka aplikace Commerce](./index.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
