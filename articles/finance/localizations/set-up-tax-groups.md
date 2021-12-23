---
title: Nastavení daňových skupin
description: Toto téma vysvětluje, jak nastavit daňové skupiny ve službě výpočtu daně.
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
ms.openlocfilehash: 50abafb958edfb8476434ff5842cd84cb186962f
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883847"
---
# <a name="set-up-tax-groups"></a>Nastavení daňových skupin

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit daňové skupiny ve službě výpočtu daně. Kromě toho se dozvíte, jak nastavit matici pravidel použitelnosti daňové skupiny a nakonfigurovat řádky v matici.

Koncept daňových skupin ve službě výpočtu daně se podobá konceptu skupin DPH v Microsoft Dynamics 365 Finance. Jsou to skupiny daňových kódů. Služba výpočtu daně používá k určení daňových kódů průnik daňové skupiny a daňové skupiny položky.

Daňové skupiny ve službě výpočtu daně se však od skupin DPH ve Finance liší tím, že nemají žádné další parametry, jako **Importní DPH** nebo **Osvobození od daně**. Místo toho jsou tyto parametry dostupné na úrovni daňového kódu.

> [!IMPORTANT]
> Nastavení daňových skupin ve službě výpočtu daně nerozlišuje právnické osoby. Toto nastavení můžete ve službě Regulatory Configuration Service (RCS) provést pouze jednou. Když ve Finance povolíte službu výpočtu daně, daňové skuiny se automaticky synchronizují pro vybranou právnickou osobu.

## <a name="set-up-a-tax-group"></a>Nastavení daňové skupiny

Podle těchto kroků nastavíte daňovou skupinu.

1. Přihlaste se ke službě [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Jdětena **Pracovní prostory** \> **Funkce globaliizace** \> **Výpočet daně**.
3. Vyberte funkci a verzi, kterou chcete nastavit, a poté vyberte **Upravit**.
4. Na kartě **Obecné** vyberte **Verze konfigurace**.
5. Na kartě **Daňová skupina** vyberte **Správa sloupce**. Pokud nastavujete daňovou skupinu poprvé, pole v dialogovém okně **Správa sloupce** se nastaví automaticky.
6. V seznamu vlevo rozbalte uzel **Řádky** a zaškrtněte políčko **Daňová skupina**.

    ![Daňová skupina vybraná v uzlu Řádky v dialogovém okně Správa sloupce.](media/select-tax-group.png)

7. Výběrem tlačítka se šipkou doprava přidejte **Daňovou skupinu** mezi **Vybrané sloupce** vpravo.

    ![Daňová skupina byla přidána do seznamu Vybrané sloupce.](media/add-tax-group.png)

8. Vyberte **OK**.

## <a name="configure-a-tax-group"></a>Konfigurace daňové skupiny

Po nastavení daňové skupiny se vytvoří matice pravidla použitelnosti daňové skupiny. Pro konfiguraci daňové skupiny můžete do matice přidat řádky.

1. Na kartě **Daňová skupina** vyberte **Přidat**.
2. Do pole **Daňová skupina** zadejte název daňové skupiny.

    > [!IMPORTANT]
    > Doporučujeme omezit název daňové skupiny na 10 znaků. Tento název je synchronizován s aplikací Finance, která má pro názvy skupin DPH limit 10 znaků.

3. V poli **Daňové kódy** zaškrtněte políčko pro každý daňový kód, který chcete zahrnout do daňové skupiny. Do jedné daňové skupiny můžete zahrnout více daňových kódů.

    ![V poli Daňové kódy je vybráno více daňových kódů.](media/multiple-tax-codes-selection.png)

4. Opakováním kroků 1 až 3 přidejte další daňové skupiny.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
