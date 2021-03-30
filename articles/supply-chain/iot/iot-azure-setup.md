---
title: Nastavení zdrojů Azure pro IoT Intelligence
description: Toto téma vysvětluje, jak vytvořit a konfigurovat zdroje Microsoft Azure, které potřebujete pro IoT Intelligence.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f728f3b5736bc7368ffb39bf2be398fb91fb373e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224947"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>Nastavení zdrojů Azure pro IoT Intelligence

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit a konfigurovat zdroje Microsoft Azure, které potřebujete pro IoT Intelligence.

## <a name="create-azure-resources"></a>Vytvoření zdrojů Azure

Takto vytvořte centrum IoT, Redis Cache a úložiště klíčů, ke kterým může přistupovat aplikace Microsoft Dynamics 365 Supply Chain Management.

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Ověření, za je ID aplikace první strany Microsoft Dynamics ERP Microservices na vašem klientovi

Chcete-li ověřit, že ID aplikace první strany pro Microsoft Dynamics ERP Microservices je na vašem klientovi, postupujte takto.

1. Přihlaste se do portálu Azure na <https://portal.azure.com>.
2. Přejděte na **Azure Active Directory**.
3. Přejděte na **Podnikové aplikace**.
4. V poli **Typ aplikace** vyberte **Aplikace společnosti Microsoft**.
5. Do pole pro vyhledávání zadejte **Microsoft Dynamics ERP Microservices**.
6. Ověřte, že je **Microsoft Dynamics ERP Microservices** v seznamu. Ostatní aplikace mají podobné názvy. Proto ověřte, že vyhledáte správnou aplikaci. ID aplikace je **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Pokud aplikace není v seznamu, musíte ji přidat ke svému klientovi:

    1. V portálu Azure na panelu nástrojů vyberte tlačítko a otevřete Azure Cloud Shell.
    2. Spusťte příkaz **Install-Module AzureAD**. Zadejte **Y** pro instalaci modulu.
    3. Spusťte příkaz **Get-InstalledModule -Name "AzureAD"** k ověření, že je modul nainstalován.
    4. Spusťte příkaz **Connect-AzureAD - Confirm** pro spuštění ověření.
    5. Spusťte příkaz **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Nyní můžete opakovat kroky 1 až 6 a ověřit, že ID aplikace je ve vašem klientovi.

### <a name="create-a-key-vault-resource"></a>Vytvoření zdroje úložiště klíčů

Při vytváření zdroje úložiště klíčů postupujte takto.

1. Na portálu Azure vytvořte nebo přejděte do skupiny zdrojů.
2. Vyberte **přidat**.
3. Na stránce **Nový** zadejte do vyhledávacího pole **Úložiště klíčů**. Pak vyberte **Vytvořit**.
4. Na stránce **Vytvoření úložiště** v poli **Úložiště klíčů** zadejte název.
5. Zkontrolujte výchozí hodnoty a poté vyberte **Zkontrolovat a vytvořit**.
6. Vyberte **Vytvořit**.

Úložiště klíčů se vytvoří na pozadí.

### <a name="create-an-iot-hub-resource"></a>Vytvoření zdroje centra IoT

Při vytváření zdroje centra IoT postupujte takto.

1. Vytvořte nebo přejděte na skupinu zdrojů.
2. Vyberte **přidat**.
3. Na stránce **Nový** zadejte do vyhledávacího pole **Centrum IoT**. Pak vyberte **Vytvořit**.
4. Do pole **Název centra IoT** zadejte název.
5. Zkontrolujte výchozí hodnoty a poté vyberte **Zkontrolovat a vytvořit**.
6. Vyberte **Vytvořit**.

Centrum IoT se vytvoří na pozadí.

> [!NOTE]
> Doporučujeme vytvořit pouze jeden zdroj centra IoT pro každé prostředí.

### <a name="create-a-redis-cache-resource"></a>Vytvoření zdroje Redis Cache

Při vytváření zdroje Redis Cache postupujte takto.

1. Vytvořte nebo přejděte na skupinu zdrojů.
2. Vyberte **přidat**.
3. Na stránce **Nový** zadejte do vyhledávacího pole **Azure Cache for Redis**. Pak vyberte **Vytvořit**.
4. Do pole **Název DNS** zadejte název.
5. Zkontrolujte výchozí hodnoty a poté vyberte **Vytvořit**.

Redis Cache se vytvoří na pozadí.

> [!NOTE]
> Doporučujeme vytvořit pouze jeden zdroj Redis Cache pro každé prostředí.

Všechny zdroje byly nyní vytvořeny.

## <a name="configure-the-azure-resources"></a>Konfigurace zdrojů Azure

### <a name="configure-the-iot-hub"></a>Konfigurace centra IoT

Pro nakonfigurování centra IoT postupujte takto.

1. Ve svých zdrojích vyberte zdroj centra IoT.
2. V levém navigačním podokně vyberte možnost **Vestavěné koncové body**.
3. Pod možností **Skupiny spotřebitelů** vložte následující skupiny spotřebitelů. Tyto skupiny spotřebitelů odpovídají vestavěným scénářům.

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>Konfigurace úložiště klíčů

Pro konfiguraci úložiště klíčů postupujte takto.

1. Ve svých zdrojích vyberte zdroj úložiště klíčů.
2. V levém navigačním podokně nalevo vyberte položku **Zásady přístupu**.
3. Vyberte **Přidat zásadu přístupu**.
4. Na stránce **Přidat zásadu přístupu** v poli **Oprávnění na základě tajných kódů** vyberte **Získat** a **Seznam**.
5. Klikněte na **Výběr objektu zabezpečení**.
6. V dialogovém okně **Objekt zabezpečení** vyhledejte a vyberte **Microsoft Dynamics ERP Microservices**. Zvolte **Vybrat**.
7. Vyberte **přidat**.
8. Zvolte **Uložit**.

Aplikace má nyní přístup k tajným klíčům v úložišti klíčů.

### <a name="save-the-iot-hub-connection-string-secret"></a>Uložení tajného klíče řetězce připojení centra IoT

Chcete-li uložit tajný klíč připojovacího řetězce centra IoT, postupujte takto.

1. Ve svých zdrojích vyberte zdroj centra IoT.
2. V levém navigačním podokně vyberte možnost **Vestavěné koncové body**.
3. Zkopírujte hodnotu do pole **Koncový bod kompatibilní s centrem událostí**.
4. Přejděte do zdroje úložiště klíčů.
5. V levém navigačním podokně vyberte položku **Tajné klíče**.
6. Vyberte **Generovat/import**.
7. Do pole **Název** zadejte název.
8. V poli **Hodnota** vložte hodnotu koncového bodu, kterou jste zkopírovali dříve.
9. Vyberte **Vytvořit**.

### <a name="save-the-redis-cache-connection-string-secret"></a>Uložení tajného klíče řetězce připojení Redis Cache

Chcete-li uložit tajný klíč připojovacího řetězce centra Redis Cache, postupujte takto.

1. Ve svých zdrojích vyberte zdroj Redis Cache.
2. Vyberte **Přístupové klíče**.
3. Zkopírujte hodnotu do pole **Primární připojovací řetězec**.
4. Přejděte do zdroje úložiště klíčů.
5. V levém navigačním podokně vyberte položku **Tajné klíče**.
6. Vyberte **Generovat/import**.
7. Do pole **Název** zadejte název.
8. V poli **Hodnota** vložte hodnotu připojovacího řetězce, kterou jste zkopírovali dříve.
9. Vyberte **Vytvořit**.

> [!NOTE]
> Kdykoli aktualizujete jeden z připojovacích řetězců, musíte také aktualizovat hodnoty tajných klíčů.

Nyní jste dokončili zřízení požadovaných zdrojů Azure. Dalším krokem je [instalace doplňku IoT Intelligence v Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]