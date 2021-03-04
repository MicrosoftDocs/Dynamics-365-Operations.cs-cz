---
title: Nastavení mapování pro pole stavu prodejní objednávky
description: Toto téma vysvětluje, jak nastavit pole stavu prodejní objednávky pro duální zápis.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 5855581100606003c1faf6b88a0ab234ae378893
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4450537"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a>Nastavení mapování pro pole stavu prodejní objednávky

[!include [banner](../../includes/banner.md)]

Pole, která označují stav prodejní objednávky, mají různé hodnoty výčtu v Microsoft Dynamics 365 Supply Chain Management a Dynamics 365 Sales. K mapování těchto polí při duálním zápisu je nutné další nastavení.

## <a name="fields-in-supply-chain-management"></a>Pole v Supply Chain Management

V aplikaci Supply Chain Management dvě pole odrážejí stav prodejní objednávky. Pole, která musíte mapovat, jsou **Stav** a **Stav dokumentu**.

Výčet **Stav** určuje celkový stav objednávky. Tento stav se zobrazuje v záhlaví objednávky.

Výčet **Stav** má následující hodnoty:

- Otevřená objednávka
- Dodáno
- Fakturováno
- Zrušeno

Výčet **Stav dokumentu** určuje nejnovější dokument, který byl vygenerován pro objednávku. Například pokud je objednávka potvrzena, tento dokument je potvrzením prodejní objednávky. Pokud je prodejní objednávka částečně vyfakturována a poté je potvrzen zbývající řádek, zůstane stav dokladu **Faktura**, protože faktura je generována později v procesu.

Výčet **Stav dokumentu** má následující hodnoty:

- Potvrzení
- Výdejka
- Dodací list
- Faktura

## <a name="fields-in-sales"></a>Pole v aplikaci Sales

V aplikaci Sales dvě pole označují stav objednávky. Pole, která musíte mapovat, jsou **Stav** a **Stav zpracování**.

Výčet **Stav** určuje celkový stav objednávky. Má následujícími hodnoty:

- Aktivní
- Odesláno
- Splněno
- Fakturováno
- Zrušeno

Výčet **Stav zpracování** byl zaveden, aby bylo možné stav přesněji mapovat pomocí aplikace Supply Chain Management.

Následující tabulka ukazuje mapování **stavu zpracování** v aplikaci Supply Chain Management.

| Stav zpracování   | Stav v Supply Chain Management | Dokument v Supply Chain Management |
|---------------------|-----------------------------------|--------------------------------------------|
| Aktivní              | Otevřená objednávka                        | Není                                       |
| Potvrzeno           | Otevřená objednávka                        | Potvrzení                               |
| Vydáno              | Otevřená objednávka                        | Výdejka                               |
| Částečně dodáno | Otevřená objednávka                        | Dodací list                               |
| Dodáno           | Dodáno                         | Dodací list                               |
| Částečně fakturováno  | Dodáno                         | Faktura                                    |
| Fakturováno            | Fakturováno                          | Faktura                                    |
| Zrušeno           | Zrušeno                         | Nelze použít                             |

Následující tabulka ukazuje mapování **stavu zpracování** mezi aplikacemi Sales a Supply Chain Management.

| Stav zpracování   | Stav v Sales | Stav v Supply Chain Management |
|---------------------|-----------------|-----------------------------------|
| Aktivní              | Aktivní          | Otevřená objednávka                        |
| Potvrzeno           | Odesláno       | Otevřená objednávka                        |
| Vydáno              | Odesláno       | Otevřená objednávka                        |
| Částečně dodáno | Aktivní          | Otevřená objednávka                        |
| Částečně fakturováno  | Aktivní          | Otevřená objednávka                        |
| Částečně fakturováno  | Splněno       | Dodáno                         |
| Fakturováno            | Fakturováno        | Fakturováno                          |
| Zrušeno           | Zrušeno       | Zrušeno                         |

## <a name="setup"></a>Nastavení

Chcete-li nastavit mapování pro pole stavu prodejní objednávky, musíte povolit atributy **IsSOPIntegrationEnabled** a **isIntegrationUser**.

Chcete-li povolit atribut **IsSOPIntegrationEnabled**, postupujte následujícím způsobem.

1. Přejděte v prohlížeči na `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Nahraďte **\<test-name\>** odkazem vaší společnosti na aplikaci Prodej.
2. Na otevřené stránce najděte **organizationid** a poznamenejte si hodnotu.

    ![Nalezení organizationid](media/sales-map-orgid.png)

3. V aplikaci Sales otevřete konzolu prohlížeče a spusťte následující skript. Použijte hodnotu **organizationid** z kroku 2.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![Kód JavaScript v konzole prohlížeče](media/sales-map-script.png)

4. Ověřte, zda je **IsSOPIntegrationEnabled** nastaveno na **true**. Použijte URL adresu z kroku 1 pro ověření hodnoty.

    ![IsSOPIntegrationEnabled nastaveno na true](media/sales-map-integration-enabled.png)

Chcete-li povolit atribut **isIntegrationUser**, postupujte následujícím způsobem.

1. V aplikaci Sales přejděte na **Nastavení \> Přizpůsobení \> Přizpůsobit systém**, vyberte **Entita uživatele** a poté otevřete **Formulář \> Uživatel**.

    ![Otevření formuláře uživatele](media/sales-map-user.png)

2. V prohlížeči polí najděte **Uživatelský režim integrace** a dvojitým kliknutím ho přidejte do formuláře. Uložte změnu.

    ![Přidání pole uživatelského režimu integrace do formuláře](media/sales-map-field-explorer.png)

3. V aplikaci Sales přejděte na **Nastavení \> Zabezpečeno \> Uživatelé** a změňte zobrazení z **Povolení uživatelé** na **Uživatelé aplikace**.

    ![Změna zobrazení z povolených uživatelů na uživatele aplikace](media/sales-map-enabled-users.png)

4. Vyberte dvě položky pro **DualWrite IntegrationUser**.

    ![Seznam uživatelů aplikací](media/sales-map-user-mode.png)

5. Změňte hodnotu pole **Uživatelský režim integrace** na **Ano**.

    ![Změna hodnoty pole uživatelského režimu integrace](media/sales-map-user-mode-yes.png)

Vaše prodejní objednávky jsou nyní mapovány.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]