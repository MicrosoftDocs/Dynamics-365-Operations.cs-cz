---
title: Konfigurace parametrů leasingu (Preview)
description: Tento článek popisuje nastavení konfigurace pro leasing majetku, například informace o zabezpečení a nastavení účetnictví.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e878fa7634cfdcc6c0db19a91e771757c545505b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895073"
---
# <a name="configure-lease-parameters"></a>Konfigurace parametrů leasingu

[!include [banner](../includes/banner.md)]

Chování leasingu majetku ovlivňuje několik nastavení konfigurace. Tato nastavení zahrnují názvy deníků, obecné parametry a nastavení profilu účtování.

1. Přejděte do nabídky **Leasing majetku \> Nastavení \> Parametry leasingu majetku**.
2. Na kartě **Leasingy** vyberte záložku s náhledem **Obecné**.

    Parametr **Povolit ruční přepsání klasifikace** určuje, zda lze klasifikaci leasingu přepsat před potvrzením platebního kalendáře.

    Parametr **Dávka mezi entitami** určuje, zda můžete odesílat provádět zaúčtování do jiných právnických osob z aktuální právnické osoby. Pokud je tento parametr zapnutý, můžete vytvořit položky deníku pro právnické osoby, ke kterým máte přístup.

3. Nastavte možnost **Povolit odstranění potvrzených leasingů** na **Ano**, aby bylo možné odstranit leasingy, které mají potvrzené platební kalendáře. Leasingy nelze odstranit, pokud jsou k nim přidruženy zaúčtované nebo nezaúčtované transakce bez ohledu na nastavení této možnosti. Po odstranění záznamu leasingu jej nemůžete obnovit. Pokud odešlete jakékoli záznamy pro odstraněný leasing, ať už ručně nebo prostřednictvím datových entit, bude se s odeslanými informacemi zacházet jako s novými, nikoli jako s aktualizací existujícího leasingu.

    Pokud nastavíte tuto možnost na **Ano** a typ přechodu knihy je **Možnost kumulativní opravy A nebo B**, systém nastaví pole **Přírůstková výpůjční úroková sazba** na hodnotu **Přírůstková výpůjční úroková sazba při přechodu** na stránce **Nastavení knihy**. Pokud je tato možnost nastavena na **Ne**, sazba předního leasingu je nastavena na hodnotu **Přírůstková výpůjční proková sazba** na stránce **Podrobnosti o knize** bez ohledu na typ přechodu knihy.

4. Nastavte možnost **Povolit stornování odpisů v uzavřené knize** na **Ano**, aby bylo možné stornovat transakce odpisových výdajů. Transakce výdajů lze stornovat, i když je kniha uzavřena.

    > [!NOTE]
    > Doporučujeme ponechat tuto možnost nastavenou na **Ne**. Nastavení této možnosti se používá jako ověření a kontrola, aby se zabránilo náhodnému odepsání verze uzavřené knihy. Ponecháním možnosti nastavenou na **Ne** pomůžete udržet přesnou zůstatkovou účetní hodnotu a přesné výpočty budoucích odpisů.

5. Nastavte možnost **Povolit rozdělení částky platby** na **Ano**, aby byl možný rozpis částek plateb na pevné záložce **Řádky splátkového kalendáře** ze stránky **Leasing**. Typy členění plateb jsou definovány v části **Nastavení** na stránce **Typy plateb částek**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
