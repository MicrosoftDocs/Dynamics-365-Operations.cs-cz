---
title: Nastavení daňových skupin položky
description: Tento článek vysvětluje, jak nastavit daňové skupiny položky ve službě výpočtu daně.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 3bc705bc8173ad2bc8ef883e6dc80b0a187314ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846456"
---
# <a name="set-up-item-tax-groups"></a>Nastavení daňových skupin položky

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak nastavit daňové skupiny položky ve službě výpočtu daně. Kromě toho se dozvíte, jak nastavit matici pravidel použitelnosti daňové skupiny položky a nakonfigurovat řádky v matici.

Koncept daňových skupin položky ve službě výpočtu daně se podobá konceptu skupin DPH položky v Microsoft Dynamics 365 Finance. Jsou to skupiny daňových kódů. Služba výpočtu daně používá k určení daňových kódů průnik daňové skupiny a daňové skupiny položky.

> [!IMPORTANT]
> Nastavení daňových skupin položky ve službě výpočtu daně nerozlišuje právnické osoby. Toto nastavení můžete ve službě Regulatory Configuration Service (RCS) provést pouze jednou. Když ve Finance povolíte službu výpočtu daně, daňové skupiny položky se automaticky synchronizují pro vybranou právnickou osobu.

## <a name="set-up-an-item-tax-group"></a>Nastavení daňové skupiny položky 

Podle těchto kroků nastavíte daňovou skupinu položky.

1. Přihlaste se ke službě [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Jdětena **Pracovní prostory** \> **Funkce globaliizace** \> **Výpočet daně**.
3. Vyberte funkci a verzi, kterou chcete nastavit, a poté vyberte **Upravit**.
4. Na kartě **Obecné** vyberte **Verze konfigurace**.
5. Na kartě **Daňová skupina položky** vyberte **Správa sloupce**. Pokud nastavujete daňovou skupinu položky poprvé, pole v dialogovém okně **Správa sloupce** se nastaví automaticky.
6. V seznamu vlevo rozbalte uzel **Řádky** a zaškrtněte políčko **Daňová skupina položky**.

    ![Daňová skupina položky vybraná v uzlu Řádky v dialogovém okně Správa sloupce.](media/select-item-tax-group.png)

7. Výběrem tlačítka se šipkou doprava přidejte **Daňovou skupinu položky** mezi **Vybrané sloupce** vpravo.

    ![Daňová skupina položky byla přidána do seznamu Vybrané sloupce.](media/add-item-tax-group.png)

8. Vyberte **OK**.

## <a name="configure-an-item-tax-group"></a>Konfigurace daňové skupiny položky

Po nastavení daňové skupiny položky se vytvoří matice pravidla použitelnosti daňové skupiny. Pro konfiguraci daňové skupiny položky můžete do matice přidat řádky.

1. Na kartě **Daňová skupina položky** vyberte **Přidat**.
2. Do pole **Daňová skupina položky** zadejte název daňové skupiny položky.

    > [!IMPORTANT]
    > Doporučujeme omezit název daňové skupiny položky na 10 znaků. Tento název je synchronizován s aplikací Finance, která má pro názvy skupin DPH položky limit 10 znaků.

3. V poli **Daňové kódy** zaškrtněte políčko pro každý daňový kód, který chcete zahrnout do daňové skupiny položky. Do jedné daňové skupiny položky můžete zahrnout více daňových kódů.

    ![V poli Daňové kódy je vybráno více daňových kódů.](media/multiple-tax-codes-selection.png)

4. Opakováním kroků 1 až 3 přidejte další daňové skupiny položky.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
