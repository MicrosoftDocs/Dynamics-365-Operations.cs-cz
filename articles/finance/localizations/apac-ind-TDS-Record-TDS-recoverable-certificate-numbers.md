---
title: Zázname čísla vratných certifikátů TDS
description: Toto téma vysvětluje, jak pomocí stránky Vratné certifikáty zaznamenat čísla a data certifikátů pro certifikáty TDS (daň odečtená u zdroje), které jsou přijímány pro konkrétního dodavatele, zákazníka nebo hlavní knihu.
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
ms.openlocfilehash: bc92a1321e6b2fe44bf7967c2aa1ad21dc353a03
ms.sourcegitcommit: dca3279a8b7cd5d0bcd4e4a3aa9938b337aa8849
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/19/2021
ms.locfileid: "7402441"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Zázname čísla vratných certifikátů TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak pomocí stránky **Vratné certifikáty** zaznamenat čísla a data certifikátů pro certifikáty TDS (daň odečtená u zdroje), které jsou přijímány pro konkrétního dodavatele, zákazníka nebo hlavní knihu. Chcete-li aktualizovat čísla a data certifikátu TDS, která jsou zaznamenána pro transakce TDS na této stránce, použijte stránku **Aktualizovat certifikát** (**Hlavní kniha \> Periodické \> Srážková daň \> Aktualizovat certifikát**). Po dokončení aktualizace čísel certifikátů TDS je zavřete.

Podle těchto pokynů zaznamenáte čísla a data certifikátu TDS.

1. Přejděte na **Daň \> Nepřímá daň \> Srážková daň \> Vratné certifikáty**.

    [![Stránka Vratné certifikáty.](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. Na stránce **Vratné certifikáty** v poli **Typ daně** vyberte **TDS**.
3. Zvolte **Nový** pro vytvoření záznamu.
4. Do pole **Číslo certifikátu** zadejte číslo certifikátu TDS.
5. V poli **Typ účtu** vyberte typ účtu, pro který je certifikát TDS přijat: **Prodejce**, **Zákazník** nebo **Hlavní kniha**.
6. V poli **Účet** vyberte číslo účtu dodavatele, zákazníka nebo hlavní knihy v závislosti na typu účtu, který jste vybrali. Pole **Název** pole zobrazuje název účtu dodavatele, zákazníka nebo hlavní knihy.
7. Do pole **Částka certifikátu** zadejte částku certifikátu TDS.
8. Do pole **Datum** zadejte datum pro číslo certifikátu.
9. Vyberte **Dotazy** k otevření stránky **Transakce s certifikáty**, kde můžete zobrazit transakce TDS, pro které je aktualizováno číslo a datum certifikátu TDS. Tyto informace lze aktualizovat na stránce **Aktualizovat certifikát** stránka (**Daň \> Přiznání \> Srážková daň \> Aktualizovat certifikát**).

    Stránka **Aktualizovat certifikát** zobrazuje následující informace pro každou transakci TDS:

    - **Datum** – datum zaúčtování transakce TDS.
    - **Doklad** – Zobrazí pro danou transakci TDS číslo dokladu.
    - **Zdroj** – Modul, ve kterém byla transakce TDS vytvořena.
    - **Účet** – Číslo účtu dodavatele, zákazníka nebo hlavní knihy, pro které byla vytvořena transakce TDS.
    - **Název** – Název účtu dodavatele, zákazníka nebo hlavní knihy, pro které byla vytvořena transakce TDS.
    - **Částka** – Částka faktury, podle které byla TDS vypočítána.
    - **Výše daně** – Částka daně TDS, která byla vypočítána pro transakci.
    - **Datum certifikátu** – Datum certifikátu TDS, které bylo aktualizováno pro transakci TDS.
    - **Číslo certifikátu** – Číslo certifikátu TDS, které bylo aktualizováno pro transakci TDS.

10. Na stránce **Vratné certifikáty** vyberte políčko **Zavřeno** k zavření čísla certifikátu TDS po dokončení jeho aktualizace pro transakce TDS na stránce **Aktualizovat certifikát**.

    Chcete-li zaškrtnout políčko **Uzavřeno** u všech záznamů na stránce, vyberte **Označit vše**.

    > [!NOTE]
    > Čísla certifikátů TDS, která je políčko **Uzavřeno** zaškrtnuté, nejsou k dispozici na stránce **Aktualizovat certifikát**.
