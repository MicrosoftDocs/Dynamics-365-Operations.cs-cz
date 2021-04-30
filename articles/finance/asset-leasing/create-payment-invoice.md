---
title: Vytvoření platebních faktur
description: Toto téma vysvětluje, jak vytvořit měsíční leasingové faktury. Můžete vytvářet faktury pro jednotlivé leasingy nebo můžete použít dávkové zpracování pro vytvoření více leasingů.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8d0b10993c61c64dadc00046907485f3886e2e01
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881173"
---
# <a name="create-payment-invoices"></a>Vytvoření platebních faktur

[!include [banner](../includes/banner.md)]

Můžete vytvářet měsíční faktury pro jednotlivé leasingy nebo můžete použít dávkové zpracování pro vytvoření více leasingů. Následující postup ukazuje, jak vytvořit samostatnou položku leasingové splátky, když he zapnutý parametr **Platba dodavateli** na stránce **Nastavení leasingové knihy**.

1. Na stránce **Shrnutí leasingu** vyberte leasing a poté vyberte **Knihy \> Platební kalendář**.
2. Vyberte platbu, kterou je třeba provést, a poté vyberte **Vytvořit deník**. Zobrazí se zpráva s oznámením, že k vybrané platbě byl vytvořen deník.
3. Vyberte **Fakturační deníky** a poté vyberte fakturu, kterou je třeba uhradit.
4. Na kartě **Řádky** zkontrolujte položku deníku, než ji zaúčtujete do hlavní knihy.

    > [!NOTE]
    > Ve výchozím nastavení řádky faktury dodavatele, které jsou vytvořeny, používají profil účtování dodavatele ze stránky **Parametry závazků**.

5. Vyberte správný deník a poté vyberte fakturu, kterou je třeba uhradit.

    V tomto příkladu je zapnutý parametr **Platba dodavateli** v leasingové knize. Faktura proto bude v deníku faktur. Sekce **Přehled** zobrazuje souhrn položky deníku a sekce **Řádky** obsahuje podrobnosti o samotných řádcích deníku.

    > [!NOTE]
    > Pokud je parametr **Platba dodavateli** vypnutý, budou položky deníku plateb uvedeny na stránce **Leasing majetku** pro leasingovou knihu a systém vytvoří položku leasingu majetku namísto faktury. Položka leasingové splátky bude zaúčtována do názvu deníku, který je zadán v poli **Deník měsíčního leasingu**.

6. Po zaúčtování transakce můžete zobrazit informace o transakci a účetní hodnotu leasingového závazku výběrem **Transakce závazku** v leasingové knize.

    V platebním kalendáři bude vybráno políčko **Deník zaúčtován** a na řádku bude uvedeno číslo deníku faktury. Po vytvoření deníku plateb a položky pro tento deník musíte záznam stornovat, než jej lze znovu vytvořit.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
