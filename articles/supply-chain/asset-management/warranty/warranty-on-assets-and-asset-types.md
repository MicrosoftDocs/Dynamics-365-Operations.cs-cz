---
title: Záruky na majetek a typy majetku
description: Tento článek vysvětluje, jak nastavit záruky na majetek a typy majetku v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2e63161aa32ecbc99baace9bb0cc649aedc600ed
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015985"
---
# <a name="warranties-on-assets-and-asset-types"></a>Záruky na majetek a typy majetku

[!include [banner](../../includes/banner.md)]

 


Tento článek vysvětluje, jak nastavit záruky na majetek a typy majetku v modulu Správa majetku.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Nastavení záruky na typ majetku

1. Vyberte **Správa majetku**\>**Nastavení**\> **Typy majetku** \>**Typy majetku**.
2. V levém podokně vyberte typ majetku, ke kterému chcete připojit záruční smlouvu dodavatele, a poté vyberte **Výchozí hodnoty typu majetku**.
3. Na pevné záložce **Obecné** v poli **Záruka dodavatele** vyberte smlouvu.

## <a name="set-up-a-warranty-on-an-asset"></a>Nastavení záruky na majetek

1. Vyberte **Správa majetku** \> **Majetek** \> **Všechen majetek**.
2. Vyberte majetek a poté zvolte **Upravit**.
3. Na pevné záložce **Dodavatel**, v oddílu **Záruka dodavatele**, v poli **Záruka** vyberte záruční smlouvu.
4. V polích **Začátek záruky** a **Konec záruky** vyberte počáteční a koncové datum.

    > [!IMPORTANT]
    > Pokud je v poli **Začátek záruky** na pracovním příkazu vybráno datum, záruka bude platit pro tento pracovní příkaz k tomuto datu. Při vytvoření pracovního příkazu je pole **Začátek záruky** automaticky nastaveno na datum vytvoření. Datum však můžete změnit tak, aby odpovídalo například počátečnímu datu záruční smlouvy.
    >
    > ![Stránka Pracovní příkaz.](media/02-warranty.png)

> [!NOTE]
> Když vytvoříte pracovní příkaz pro majetek, který je pokryt záruční smlouvou dodavatele, a pokud má pracovní příkaz očekávané počáteční datum během záruční doby, obdržíte oznámení o záruční smlouvě. Poté můžete požadovaný pracovní příkaz zrušit podle potřeby.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]