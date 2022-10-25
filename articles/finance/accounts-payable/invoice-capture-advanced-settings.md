---
title: Pokročilá nastavení řešení Invoice Capture
description: Tento článek poskytuje informace o pokročilých nastaveních v řešení Invoice Capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691138"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Pokročilá nastavení řešení Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tento článek poskytuje informace o pokročilých nastaveních v řešení Invoice Capture.

## <a name="create-additional-connections-for-channels"></a>Vytvořte další připojení pro kanály

Musíte vytvořit připojení k e-mailu nebo úložišti souborů, abyste mohli sledovat příchozí faktury z různých kanálů. Chcete-li udělit přístup pro automatizované toky, které se v řešení používají, musíte připojení zaregistrovat na začátku.

K importu faktur se používají následující typy připojení:

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

Kanál pro import faktur použije připojení v dalších konfiguračních krocích. Než mohou uživatelé vytvořit kanál konkrétního připojení, musí jim být udělena role zabezpečení **Správce** a musí vytvářet spojení.

Pokud chcete vytvořit připojení k Microsoft Dataverse, postupujte takto.

1. Přejděte na **Systém správce \> Výchozí řešení**.
2. Vyberte **Nový** a pak vyberte **Informace o připojení**.
3. Do pole **Zobrazované jméno** zadejte název.
4. Jako konektor vyberte **Microsoft Dataverse**.
5. Pokud nastavujete připojení poprvé, vyberte **Nové připojení**.
6. V dialogovém okně, které se zobrazí, vytvořte připojení Dataverse a pak vyberte **Vytvořit**.
7. Zadejte účet Dataverse a heslo.
8. Po úspěšném ověření přejděte na stránku připojení a vyberte **Obnovit**, vyberte účet a poté vyberte **Vytvořit**.

Chcete-li vytvořit e-mail nebo připojení k úložišti souborů, postupujte následujícím způsobem.

1. Na stránce **Vytvoření spojení** v poli **Typ připojení** vyberte **Office 365 Outlook**.
2. Pro e-mailové připojení můžete vybrat **Outlook.com** nebo **Office 365 Outlook** jako konektor. Pro připojení úložiště souborů můžete vybrat buď **OneDrive** nebo **SharePoint**.

Chcete-li zkontrolovat stávající připojení, přejděte na **Výchozí řešení \> Objekty \> Informace o připojení**. Uživatel, který vytváří kanály, by měl mít alespoň jedno Dataverse připojení vedle konkrétních připojení e-mailu nebo úložiště souborů. Tvůrce nového kanálu by měl být vlastníkem připojení.
