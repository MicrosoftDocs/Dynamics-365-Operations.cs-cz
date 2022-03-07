---
title: Nastavení platebních poplatků pro platby autoritě TDS
description: Toto téma vysvětluje, jak nastavit poplatky za platby, které se účtují za platby autority pro daně odečtené u zdroje (TDS).
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
ms.openlocfilehash: 9213827ea1ad342beb7ac2fe586606651cfdcfa1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358427"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>Nastavení platebních poplatků pro platby autoritě TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit poplatky za platby, které se účtují za platby autority pro daně odečtené u zdroje (TDS).

1. Přejděte do nabídky **Závazky \> Nastavení platby \> Platební poplatek**.

    [![Stránka Platební poplatek.](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Vybráním možnosti **Nové** vytvořte platební poplatek a poté zadejte požadované informace.
3. V poli **Typ poplatku** vyberte typ platebního poplatku.

    - **Není**
    - **Úrok** – Úroky jsou účtovány za pozdní platby, které jsou provedeny dodavateli autority TDS.
    - **Jiné** – Jiné platby jsou účtovány za pozdní platby, které jsou provedeny dodavateli autority TDS.

    Pokud vyberete **Úrok** nebo **Ostatní**, pole **Účtovat** je automaticky nastaveno na **Hlavní kniha**.

4. Pokud jste vybrali **Úrok** nebo **Ostatní** v poli **Typ pole**, v poli **Hlavní účet** vyberte účet hlavní knihy, do kterého chcete zaúčtovat úrok nebo jiné poplatky.
5. Zadejte další požadované údaje.
6. V podokně Akce vyberte **Nastavení platebního poplatku** k otevření stránky **Nastavení platebního poplatku**, kde můžete nastavit poplatky za platby pro různé kombinace bank, způsobů plateb, platebních podmínek, měn a časových intervalů.

    [![Stránka Nastavení platebních poplatků.](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. Na kartě **Přehled** v poli **Seskupení** uveďte, u kterých bank nastavujete poplatek za platbu:

    - **Tabulka** – Poplatek platí pro konkrétní bankovní účet.
    - **Skupina** – Poplatek platí pro konkrétní skupinu bank.
    - **Vše** – Poplatek je platný pro všechny bankovní účty.

8. Pokud jste vybrali **Tabulka** nebo **Skupina** v poli **Seskupení**, v poli **Bankovní relace** vyberte konkrétní bankovní účet nebo bankovní skupinu, pro kterou nastavujete poplatek za platbu.
9. V poli **Metoda platby** vyberte metodu platby, která má být použita pro platbu platebního poplatku.
10. V poli **Specifikace platby** vyberte nebo zadejte kód specifikace platby, který byl vygenerován na stránce **Specifikace platby**.
    - Specifikace platby se používají pro platbu metodou elektronického převodu finančních prostředků.
12. V poli **Měna platby** vyberte měnu, která poplatek aktivuje. Poplatek mohou aktivovat pouze transakce, které používají vybranou měnu. Pokud toto pole nevyplníte, všechny měny aktivují poplatek.
13. V poli **Procento/částka** vyberte metodu výpočtu. Možnosti jsou **Částka**, **Procento** a **Interval**.
14. Do pole **Částka poplatku** zadejte částku poplatku jako procento platby nebo částku za jednu platbu.
15. V poli **Měna poplatku** zadejte kód měny pro poplatek.
16. Vyberte kartu **Všeobecné** k zobrazení nebo úpravě údajů vybraného bankovního účtu.

    [![Karta Obecné.](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. Do pole **Minimum** zadejte minimální částku transakce, která aktivuje poplatek.
17. Do pole **Maximum** zadejte maximální částku transakce, která aktivuje poplatek.
18. V polích **Od data** a **K datu** definujte časové období pro výpočet poplatků.
19. Do pole **Minimální poplatek** zadejte částku poplatku jako procento platby nebo částku za jednu platbu.
20. Do pole **Skupina DPH** vyberte skupinu DPH, která se má použít k výpočtu DPH pro částku poplatku.
21. Do pole **Skupina DPH položky** vyberte skupinu DPH položky, která se má použít k výpočtu DPH položky pro částku poplatku.
22. Vyberte kartu **Interval**. 

    [![Karta Interval.](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. Do pole **Dny** zadejte počet dní mezi datem zaúčtování (datem slevy) platby a datem splatnosti vlastní směnky.
24. V poli **Procento/částka** vyberte, zda je specifikace procentem nebo stanovenou částkou.
25. Do pole **Částka poplatku** zadejte částku poplatku jako procento platby nebo částku za jednu platbu.
26. Zavřete stránku **Nastavení platebního poplatku**.
27. Zavřete stránku **Platební poplatek**.
