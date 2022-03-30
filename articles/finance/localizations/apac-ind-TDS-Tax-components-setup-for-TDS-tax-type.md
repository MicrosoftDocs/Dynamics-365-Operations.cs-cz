---
title: Nastavení složek daně pro typ daně TDS
description: Toto téma vysvětluje, jak nastavit složky srážkové daně pro daňový typ se srážkou daně u zdroje (TDS). Vysvětluje také, jak definovat prahovou hranici, která se používá k výpočtu TDS pro každou složku TDS.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 34ef487da382e50efb2f9637d537669524c25d8f
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408058"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>Nastavení složek daně pro typ daně TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit složky srážkové daně pro daňový typ se srážkou daně u zdroje (TDS). Složky TDS jsou TDS, příplatek, PE-Cess a SHE Cess. Toto téma vysvětluje, jak definovat prahovou hranici, která se používá k výpočtu TDS pro každou složku TDS. Dále můžete definovat prahovou hodnotu výjimky, která se používá k výpočtu TDS pro každou složku TDS.

Chcete-li nastavit složky TDS, postupujte následujícím způsobem:

1. Přejděte do nabídky **Daň \> Nastavení \> Srážková daň \> Složky srážkové daně**.

    [![Stránka Složky srážkové daně.](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. V poli **Typ daně** vyberte **TDS** a nastavte složky srážkové daně pro typ daně TDS.
3. V podokně Akce vyberte možnost **Nový** a vytvořte řádek.
4. Do pole **Složka srážkové daně** zadejte název složky TDS.
5. V poli **Skupina složek srážkové daně** vyberte skupinu složek TDS srážkové daně, ke které chcete složku TDS připojit.
6. Na pevné záložce **Obecné** v poli **Popis** zadejte popis složky TDS.
7. V podokně akcí vyberte **Mezní hodnota** k otevření stránky **Mezní hodnota** stránka, abyste mohli definovat mezí hodnotu, která se použije pro výpočet TDS pro složku TDS.
8. Použijte pole **Od data** a **Do data** k definování období, na které se prahová hodnota vztahuje.
9. Na rychlé kartě **Všeobecné** do pole **Mezní hodnota** zadejte mezní hodnotu, která se použije pro výpočet TDS pro komponentu TDS. Daň bude odečtena u zdroje, pouze pokud kumulativní částka faktury překročí prahovou hodnotu.

    Například pokud je prahová částka 10 000, TDS se vypočítá poté, co kumulativní částka faktury přesáhne 10 000 (jinými slovy, když je to 10 001 nebo více).

10. Do pole **Mezní hodnota výjimky** zadejte mezní hodnotu výjimky, která se použije pro výpočet TDS pro komponentu TDS. Daň na řádku faktury bude odečtena u zdroje, pouze pokud faktury překročí prahovou hodnotu výjimky.

    Například pokud je prahová hodnota pro výjimku 5000, TDS se vypočítá na konkrétním řádku faktury, pokud částka faktury přesáhne 5000 (jinými slovy, pokud je to 5001 nebo více).

    [![Stránka Mezní hodnota.](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > Výše mezní hodnoty výjimky musí být menší nebo rovna mezní hodnotě.
    >
    > Daň se odečte za transakci, pokud částka transakce překročí mezní hodnotu pro výjimku, i když kumulativní částka faktury nepřekročí mezní hodnotu uvedenou v poli **Mezní hodnota**.

11. Zavřete stránku **Mezní hodnota** pro návrat na stránku **Složky srážkové daně**.
12. V podokně akcí vyberte **Kopírovat** k otevření dialogového okna **Zkopírovat složky srážkové daně**, abyste mohli zkopírovat složky TDS, které byly nastaveny pro jednu skupinu složek TDS, do jiné skupiny složek TDS.
13. V poli **Z** vyberte skupinu složek TDS, ze které chcete kopírovat složky TDS. V poli **Do** vyberte skupinu složek srážkové daně, do které chcete kopírovat složky TDS.

    > [!NOTE]
    > Společné složky TDS, které jsou připojeny k oběma skupinám složek TDS, se nekopírují.

14. Vyberte **OK** ke zkopírování a vytvoření složek TDS pro další skupinu složek TDS na stránce **Složky srážkové daně**.

    [![Dialogové okno Zkopírovat složky srážkové daně.](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. Zavřete stránku.
