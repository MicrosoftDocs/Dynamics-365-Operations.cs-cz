---
title: Maloobchod se neobjevuje v seznamu obchodů, ze kterých si můžete vyzvednout
description: Tento článek poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se maloobchod neobjeví v seznamu obchodů, kde lze vyzvednout položky.
author: Reza-Assadi
ms.date: 03/11/2021
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
ms.openlocfilehash: 936b3df3194fbdacf8e853ed60431b077f4015cd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905249"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Maloobchod se neobjevuje v seznamu obchodů, ze kterých si můžete vyzvednout

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se maloobchod neobjeví v seznamu obchodů, kde lze vyzvednout položky.

## <a name="description"></a>popis

Maloobchod se neobjevuje v seznamu obchodů, kde lze zboží vyzvednout.

## <a name="resolution"></a>Rozlišení

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>Konfigurace zeměpisné délky a šířky pro adresu obchodu v centrále Commerce

Pro konfiguraci zeměpisné délky a šířky pro adresu obchodu v centrále Commerce postupujte následovně.

1. Přejděte na **Retail a Commerce \> Kanály \> Obchody \> Všechny obchody**.
1. Mezi možnostmi vyzvednutí na webu elektronického obchodování vyhledejte obchod, který chcete zobrazit. Poznamenejte si jeho hodnotu **Číslo provozní jednotky**.
1. Přejděte do nabídky **Správa organizace \> Organizace \> Provozní jednotky**.
1. Vyhledejte číslo provozní jednotky, které jste si dříve poznamenali, a poté vyberte provozní jednotku ve výsledcích hledání.
1. Na pevné záložce **Adresy** vyberte **Další možnosti** a poté vyberte **Rozšířené**.
1. Na pevné záložce **Všeobecné** zkontrolujte, že jsou správně nastavena pole **Zeměpisná délka** a **Zeměpisná šířka**. V rámci tohoto kroku zkontrolujte, zda jsou hodnoty správně zadány jako kladná nebo záporná čísla.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Konfigurace skupin plnění v centrále Commerce

Konfiguraci skupin plnění v centrále Commerce provedete následovně.

1. Přejděte na **Retail a Commerce \> Kanály \> Online obchody**.
1. Vyberte online obchod, který chcete konfigurovat.
1. V podokně Akce vyberte kartu **Nastavení** a poté vyberte možnost **Přiřazení skupiny plnění**.
1. Na stránce **Přiřazení skupiny plnění** vyberte skupinu plnění pro online obchod.
1. V části **Nastavení** zkontrolujte, že maloobchod je správně nakonfigurován pro skupinu plnění.

## <a name="additional-resources"></a>Další prostředky 

[Vytvoření provozní jednotky](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[Nastavení online kanálu](../channel-setup-online.md)