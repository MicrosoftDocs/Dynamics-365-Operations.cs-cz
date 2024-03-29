---
title: Vytvoření platebních faktur
description: Tento článek vysvětluje, jak vytvořit měsíční leasingové faktury. Můžete vytvářet faktury pro jednotlivé leasingy nebo můžete použít dávkové zpracování pro vytvoření více leasingů.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0ac9efaf6d068377053ae36951f4ad808fcb2438
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886395"
---
# <a name="create-payment-invoices"></a>Vytvoření platebních faktur

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Můžete vytvářet měsíční faktury pro jednotlivé leasingy nebo můžete použít dávkové zpracování pro vytvoření více leasingů. Následující postup ukazuje, jak vytvořit samostatnou položku leasingové splátky, když he zapnutý parametr **Platba dodavateli** na stránce **Nastavení leasingové knihy**.

1. Na stránce **Shrnutí leasingu** vyberte leasing a poté vyberte **Knihy \> Platební kalendář**.
2. Vyberte platbu, kterou je třeba provést, a poté vyberte **Vytvořit deník**. Zobrazí se zpráva s oznámením, že k vybrané platbě byl vytvořen deník.
3. Vyberte **Fakturační deníky** a poté vyberte fakturu, kterou je třeba uhradit.
4. Na kartě **Řádky** zkontrolujte položku deníku, než ji zaúčtujete do hlavní knihy.

    > [!NOTE]
    > Ve výchozím nastavení řádky faktury dodavatele, které jsou vytvořeny, používají profil účtování dodavatele ze stránky **Parametry závazků**.

5. Vyberte správný deník a poté vyberte fakturu, kterou je třeba uhradit.

    V tomto příkladu je zapnutý parametr **Platba dodavateli** v leasingové knize. Faktura proto bude v deníku faktur. Sekce **Přehled** zobrazuje souhrn položky deníku a sekce **Řádky** obsahuje podrobnosti o samotných řádcích deníku.
    
   Systém zablokuje úpravu určitých finančních polí, aby se zabránilo jakýmkoli odchylkám mezi transakcemi a plány. Mezi zamčená pole patří: **Účet**, **Množství**, **Finanční dimenze**, **Měna** a **Typ transakce**. Kromě toho nebudete moci přidávat ani odstraňovat řádky záznamů deníku v žádných položkách deníku leasingu majektu, protože to může způsobit odchylky mezi plány a transakcemi.

    > [!NOTE]
    > Pokud je parametr **Platba dodavateli** vypnutý, budou položky deníku plateb uvedeny na stránce **Leasing majetku** pro leasingovou knihu a systém vytvoří položku leasingu majetku namísto faktury. Položka leasingové splátky bude zaúčtována do názvu deníku, který je zadán v poli **Deník měsíčního leasingu**.

6. Po zaúčtování transakce můžete zobrazit informace o transakci a účetní hodnotu leasingového závazku výběrem **Transakce závazku** v leasingové knize.

    V platebním kalendáři bude vybráno políčko **Deník zaúčtován** a na řádku bude uvedeno číslo deníku faktury. Po vytvoření deníku plateb a položky pro tento deník musíte záznam stornovat, než jej lze znovu vytvořit.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
