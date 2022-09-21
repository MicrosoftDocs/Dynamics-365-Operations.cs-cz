---
title: Parametry Sensor Data Intelligence
description: Tento článek poskytuje informace o konfiguračních nastaveních, která jsou k dispozici na stránce parametrů Sensor Data Intelligence.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 4a6665cc078e54da4ebb7920ec8826352ab7a816
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428317"
---
# <a name="sensor-data-intelligence-parameters"></a>Parametry Sensor Data Intelligence

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Stránka **Parametry Sensor Data Intelligence** obsahuje několik nastavení, která můžete použít ke konfiguraci funkce. Tato nastavení zahrnují parametry připojení Azure a parametr pro dobu trvání výstražných zpráv, které se odesílají uživatelům v reakci na měření senzorů.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Přečtěte si a změňte údaje připojení pro vaše řešení Azure IoT

Obvykle nastavíte řešení Azure IoT a připojíte ho k Microsoft Dynamics 365 Supply Chain Management ze stránky **Nasadit a připojit prostředky Azure**, která vás provede oběma postupy. (Další informace viz [Nasazení řešení IoT v Azure](sdi-deploy-iot-solution-on-azure.md).) Podrobnosti o připojení můžete také kdykoli zobrazit a upravit v Supply Chain Management podle následujících kroků.

1. Přejděte na **Správa systému \> Nastavení \> Sensor Data Intelligence \> Parametry Sensor Data Intelligence**.
1. Na kartě **Časové řady** v poli **Připojovací řetězec úložiště metriky Redis** zadejte hodnotu **Primární připojovací řetězec (StackExchange.Redis)** pro řešení Azure IoT, ke kterému se chcete připojit. Další informace o tom, jak tuto hodnotu zjistit, viz [Nasazení řešení IoT v Azure](sdi-deploy-iot-solution-on-azure.md).
1. Na kartě **Integrace** v poli **ID klienta aplikace Azure AD** zadejte hodnotu **ID klienta** pro řešení Azure IoT, ke kterému se chcete připojit. Další informace o tom, jak tuto hodnotu zjistit, viz [Nasazení řešení IoT v Azure](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Nastavení životnosti výstražných zpráv

Pokaždé, když Sensor Data Intelligence detekuje situaci, která vyžaduje pozornost uživatele, odešle příslušnému uživateli upozornění. Chcete-li zabránit hromadění těchto oznámení v systému, měli byste nastavit jejich platnost po několika dnech.

1. Přejděte na **Správa systému \> Nastavení \> Sensor Data Intelligence \> Parametry Sensor Data Intelligence**.
1. Na kartě **Oznámení** do pole **Dny platnosti oznámení** zadejte počet dní pro uchování oznámení. Po uplynutí stanovené doby bude oznámení smazáno.
