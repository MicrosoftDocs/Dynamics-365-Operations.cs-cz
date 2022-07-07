---
title: Příchozí a odchozí majetek
description: Tento článek vysvětluje, jak registrovat příchozí a odchozí majetek v modulu Správa majetku.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd7482cfe943347840e9fb070151d66fbe5ef9ca
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016529"
---
# <a name="inbound-and-outbound-assets"></a>Příchozí a odchozí majetek

[!include [banner](../../includes/banner.md)]

 

Pokud vaše společnost provádí úlohy oprav nebo údržby u majetku, který byl přijat z jiných míst nebo od jiných zákazníků, může správa majetku sledovat jak vstupní majetek, který je na cestě do vaší firmy, a příchozí majetek, který se vrací.

> [!NOTE]
> Pokud chcete použít příchozí a odchozí stavy životního cyklu pro správu majetku, který přichází nebo se vrací, musíte pro podporu těchto akcí nastavit stavy životního cyklu požadavků na údržbu a modely životního cyklu. Další informace naleznete v tématu [Požadavky na údržbu](/d365F-O/supply-chain/asset-management/manage-maintenance-requests/../manage-maintenance-requests/maintenance-request-overview).

Nastavení správy majetku určuje, zda můžete pracovat s příchozím nebo odchozím majetkem.

## <a name="register-assets-as-inbound"></a>Registrace majetku jako příchozího

1. Vyberte **Správa majetku** \> **Požadavky na údržbu** \> **Aktivní požadavky na údržbu**.
2. Zvolte požadavek na údržbu.
3. Zvolte **Aktualizovat stav požadavku na údržbu**.
4. Vyberte **Příchozí** (nebo jiný stav životního cyklu, který jste vytvořili pro příchozí majetek) a pak zvolte **OK**.

![Registrace majetku jako příchozího.](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Registrace příchozího majetku jako přijatého

1. Vyberte **Správa majektu** \> **Příchozí/odchozí** \> **Příchozí majetek**.
2. Zvolte majetek nebo požadavek na údržbu.
3. Zvolte **Přijmout majetek**.
4. V poli **Přijato** zadejte datum a čas. Pak vyberte **OK**. Záznam bude odebrán ze stránky se seznamem **Příchozí majetek**.

![Registrace příchozího majetku jako přijatého.](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Registrace majetku jako odchozího

Po dokončení úlohy údržby nebo opravy můžete majetek zaregistrovat jako vrácený.

1. Vyberte **Správa majetku** \> **Požadavky na údržbu** \> **Aktivní požadavky na údržbu**.
2. Zvolte požadavek na údržbu.
3. Zvolte **Aktualizovat stav požadavku na údržbu**.
4. Vyberte **Odchozí** (nebo jiný stav životního cyklu, který jste vytvořili pro odchozí majetek) a pak zvolte **OK**.

## <a name="register-outbound-assets-as-delivered"></a>Registrace odchozího majetku jako doručeného

1. Vyberte **Správa majektu** \> **Příchozí/odchozí** \> **Odchozí majetek**.
2. Zvolte majetek nebo požadavek na údržbu.
3. Vyberte **Doručit majetek**.
4. V poli **Doručeno** zadejte datum a čas. Pak vyberte **OK**. Záznam bude odebrán ze stránky se seznamem **Odchozí majetek**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]