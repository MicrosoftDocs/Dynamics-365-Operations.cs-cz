---
title: Aktualizace čísel a dat certifikátu pro transakce TDS
description: Toto téma vysvětluje, jak aktualizovat čísla a data vratných certifikátů, které byly zaznamenány pro účet dodavatele, zákazníka hlavní knihy a pro daň odečtenou u zdroje (TDS).
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
ms.openlocfilehash: b23f01f110009ba2f0cfe71c7bb995a4dc21ca3b
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408273"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>Aktualizace čísel a dat certifikátu pro transakce TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak aktualizovat čísla a data vratných certifikátů, které byly zaznamenány pro účet dodavatele, zákazníka hlavní knihy a pro daň odečtenou u zdroje (TDS). Certifikáty pro transakce TDS si můžete prohlédnout na stránce **Vratné certifikáty**. Certifikáty můžete aktualizovat pomocí stránky **Aktualizovat certifikáty** .

Podle těchto pokynů aktualizujete čísla a data certifikátu pro transakci TDS.

1. Přejděte do nabídky **Daň \> Přiznání \> Srážková daň \> Aktualizovat certifikát**.

    [![Stránka Aktualizovat certifikát.](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. Na stránce **Aktualizovat certifikát** v části **Vybrat** v poli **Typ daně** vyberte **TDS**.
3. V poli **Číslo certifikátu** vyberte číslo certifikátu TDS zákazníka nebo dodavatele.

    > [!NOTE]
    > Pole **Číslo certifikátu** uvádí pouze čísla certifikátů TDS, pro která je políčko **Uzavřeno** nezaškrtnuté na stránce **Vratné certifikáty**.

    Pole **Datum certifikátu** zobrazuje datum certifikátu. Pole **Typ účtu** zobrazuje typ účtu, pro který je přijato číslo certifikátu TDS, a pole **Název** zobrazuje název účtu.

5. V polích **Od data** a **Do data** vyberte počáteční a koncová data období, pro která se mají zobrazit transakce TDS.
6. Vyberte **Zobrazit data** k zobrazení transakcí TDS, které byly zaúčtovány během vybraného období.

    Na kartě **Přehled**, mřížka v horním podokně zobrazuje následující informace o každé transakci TDS, která byla zaúčtována pro dodavatele nebo zákazníka během vybraného období:

    - **Doklad** – Zobrazí pro danou transakci TDS číslo dokladu.
    - **Datum** – datum transakce TDS.
    - **Částka** – Částka faktury, podle které byla TDS vypočítána.
    - **Výše daně** – Částka daně TDS, která byla vypočítána pro transakci.

7. Chcete-li přesunout konkrétní transakce TDS z horní mřížky do dolní mřížky, vyberte transakce a poté vyberte **Zahrnout**. Případně vyberte **Zahrnout vše** a přesuňte všechny transakce TDS z horní mřížky do spodní mřížky.

    Chcete-li přesunout konkrétní transakce TDS nebo všechny transakce TDS ze spodní mřížky do horní mřížky, použijte tlačítka **Vyloučit** nebo **Vyloučit vše**.

8. Vyberte **Aktualizovat** k aktualizaci polí **Číslo certifikátu** a **Datum certifikátu** pro transakce TDS ve spodní mřížce.
10. Přejděte na **Daň \> Nepřímé daně \> Srážková daň \> Vratný certifikát** a vyberte **Poptávka** pro zobrazení aktualizovaných řádků transakcí, které mají na certifikátu nová čísla certifikátů na stránce **Transakce s certifikáty**.

    [![Stránka Transakce s certifikátem.](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
