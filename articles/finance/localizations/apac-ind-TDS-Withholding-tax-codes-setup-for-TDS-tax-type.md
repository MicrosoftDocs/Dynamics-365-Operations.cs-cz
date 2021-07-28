---
title: Nastavení kódů srážkové daně pro typy daně TDS
description: Toto téma vysvětluje, jak nastavit kódy daně odečtené u zdroje (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 57de382c6d363a6c1d87cf734e9aedb32d6009a9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349921"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>Nastavení kódů srážkové daně pro typy daně TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit kódy daně odečtené u zdroje (TDS).

1. Přejděte na **Daň \> Nepřímé daně \> Srážková daň \> Kódy srážkové daně**.

    [![Stránka Kódy srážkové daně.](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. V podokně akcí vyberte **Nový** pro vytvoření kódu srážkové daně pro TDS a zadejte požadované podrobnosti.
3. Na pevné záložce **Obecné** v poli **Typ daně** vyberte **TDS** ke kategorizaci kódu daně jako kódu daně TDS.
4. V poli **Období vypořádání** vyberte období vypořádání TDS pro kód daně TDS.
5. V poli **Hlavní účet** vyberte účet hlavní knihy, na který by měla být zaúčtována částka TDS.
6. V poli **Pohledávka** vyberte pohledávku, na kterou má být zaúčtována částka TDS odečtená v prodejních transakcích.

    Pole **Původ** je automaticky nastaveno na hodnotu **Procento z hrubé částky**, kterou nelze změnit.

    > [!NOTE]
    > Nemůžete nastavit původ na **Procento čisté částky** pro daňové kódy typu daně TDS.

7. V poli **Komponenta srážkové daně** vyberte skupinu komponent srážkové daně pro kód daně TDS.
8. V podokně akcí vyberte **Hodnoty** k otevření stránky **Hodnoty srážkové daně**.
9. V poli **Od data** zadejte počáteční datum pro hodnotu TDS. V poli **Do data** zadejte koncové datum.

    > [!NOTE]
    > Pole **Minimální limit**, **Horní limit** a **% vyloučení** nejsou k dispozici pro daňové kódy typu daně TDS.

10. V poli **Hodnota** zadejte procento TDS používané pro kód daně TDS.
11. Zavřete stránku **Hodnoty srážkové daně** pro návrat na stránku **Kódy srážkové daně**.

    > [!NOTE]
    > Tlačítko **Limity** na stránce **Kódy srážkové daně** není k dispozici pro daňové kódy typu daně TDS.

12. Zavřete stránku.
