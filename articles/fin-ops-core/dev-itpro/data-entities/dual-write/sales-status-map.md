---
title: Nastavení mapování pro sloupce stavu prodejní objednávky
description: Toto téma vysvětluje, jak nastavit sloupce stavu prodejní objednávky pro duální zápis.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6eafd9b14d02dec3455b73aeee1264629331a57b8ce760b7db6f6ddbaa7406b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741647"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>Nastavení mapování pro sloupce stavu prodejní objednávky

[!include [banner](../../includes/banner.md)]

Sloupce, které označují stav prodejní objednávky, mají různé hodnoty výčtu v Microsoft Dynamics 365 Supply Chain Management a Dynamics 365 Sales. K mapování těchto sloupců při duálním zápisu je nutné další nastavení.

## <a name="columns-in-supply-chain-management"></a>sloupce v Supply Chain Management

V aplikaci Supply Chain Management dva sloupce odrážejí stav prodejní objednávky. Sloupce, které musíte mapovat, jsou **Stav** a **Stav dokumentu**.

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

## <a name="columns-in-sales"></a>sloupce v aplikaci Prodej

V aplikaci Sales dva sloupce označují stav objednávky. Sloupce, které musíte mapovat, jsou **Stav** a **Stav zpracování**.

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

Chcete-li nastavit mapování pro sloupce stavu prodejní objednávky, musíte povolit atributy **IsSOPIntegrationEnabled** a **isIntegrationUser**.

Chcete-li povolit atribut **IsSOPIntegrationEnabled**, postupujte následujícím způsobem.

1. Přejděte v prohlížeči na `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Nahraďte **\<test-name\>** odkazem vaší společnosti na aplikaci Prodej.
2. Na otevřené stránce najděte **organizationid** a poznamenejte si hodnotu.

    ![Nalezení organizationid.](media/sales-map-orgid.png)

3. V aplikaci Sales otevřete konzolu prohlížeče a spusťte následující skript. Použijte hodnotu **organizationid** z kroku 2.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![Kód JavaScript v konzole prohlížeče.](media/sales-map-script.png)

4. Ověřte, zda je **IsSOPIntegrationEnabled** nastaveno na **true**. Použijte URL adresu z kroku 1 pro ověření hodnoty.

    ![IsSOPIntegrationEnabled nastaveno na true.](media/sales-map-integration-enabled.png)

Chcete-li povolit atribut **isIntegrationUser**, postupujte následujícím způsobem.

1. V aplikaci Sales přejděte na **Nastavení \> Přizpůsobení \> Přizpůsobit systém**, vyberte **Tabulka uživatele** a poté otevřete **Formulář \> Uživatel**.

    ![Otevření formuláře uživatele.](media/sales-map-user.png)

2. V prohlížeči polí najděte **Uživatelský režim integrace** a dvojitým kliknutím ho přidejte do formuláře. Uložte změnu.

    ![Přidání sloupce uživatelského režimu integrace do formuláře.](media/sales-map-field-explorer.png)

3. V aplikaci Sales přejděte na **Nastavení \> Zabezpečeno \> Uživatelé** a změňte zobrazení z **Povolení uživatelé** na **Uživatelé aplikace**.

    ![Změna zobrazení z povolených uživatelů na uživatele aplikace.](media/sales-map-enabled-users.png)

4. Vyberte dvě položky pro **DualWrite IntegrationUser**.

    ![Seznam uživatelů aplikací.](media/sales-map-user-mode.png)

5. Změňte hodnotu sloupce **Uživatelský režim integrace** na **Ano**.

    ![Změna hodnoty sloupce uživatelského režimu integrace.](media/sales-map-user-mode-yes.png)

Vaše prodejní objednávky jsou nyní mapovány.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]