---
title: Začínáme se správou služby doplňky elektronické fakturace
description: Toto téma poskytuje informace, jak začít s doplňkem elektronické fakturace.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104353"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>Začínáme se správou služby doplňky elektronické fakturace

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Předpoklady

Než provedete postupy v tomto tématu, musí být splněny následující předpoklady:

- Musíte mít přístup ke svému účtu Microsoft Dynamics Lifecycle Services (LCS).
- Musíte mít projekt LCS, který obsahuje verzi 10.0.13 nebo novější nástroje Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management. Kromě toho musí být tyto aplikace nasazeny v jedné z následujících geografických oblastí Azure:

    - Východní USA
    - USA – západ
    - Sever EU
    - Západ EU

- Musíte mít přístup ke svému účtu Dynamics 365 Regulatory Configuration Services (RCS).
- Musíte aktivovat funkci Globalizace pro svůj účet RCS v modulu Správa funkcí. Pro více informací viz [Regulatory Configuration Services (RCS) - funkce globalizace](rcs-globalization-feature.md).
- Musíte vytvořit trezor klíčů a účet úložiště Azure. Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>Nainstalujte doplněk pro mikroslužby ve službě Lifecycle Services

1. Přihlaste se k účtu LCS.
2. Vyberte dlaždici **Náhled správy funkcí**.
3. V části **Funkce Public Preview** vyberte **služba elektronické fakturace**.
4. Ujistěte se, zda je možnost **Funkce Preview zapnuta** nastavena na hodnotu **Ano**.

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>Nastavení parametrů pro integraci RCS s doplňkem elektronické fakturace

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Elektronické výkaznictví** v části **Související odkazy** vyberte **Parametry elektronického výkaznictví**.
3. Na kartě **Služba elektronické fakturace** v poli **Identifikátor URI koncového bodu služby** zadejte příslušný koncový bod služby pro vaši geografii Azure, jak je znázorněno v následující tabulce.

    | Geografie datového centra Azure | URI adresa koncového bodu služby                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Východní USA                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | USA – západ                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Sever EU                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Západ EU                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. Ověřte, zda je pole **Id aplikace** nastaveno na **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Tato hodnota je pevná hodnota.
5. V poli **ID prostředí LCS** zadejte ID účtu předplatného LCS.
6. Zvolte **Uložit** a pak zavřete stránku.

## <a name="create-key-vault-secret"></a>Vytvoření tajného kódu Key Vault

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Elektronická fakturace**.
3. Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby** a potom vyberte **Parametry Key Vault**.
4. Vyberte možnost **Nový** k vytvoření tajného kódu trezoru klíčů.
5. Do pole **Název** zadejte název tajného kódu trezoru klíčů. Zadejte popis do pole **Popis**.
6. Do pole **Identifikátoru URI Key Vault** vložte tajný kód z Azure Key Vault.
7. Zvolte **Uložit**.

## <a name="create-storage-account-secret"></a>Vytvoření tajného kódu účtu úložiště

1. Na stránce **Parametry trezoru klíčů** v části **Certifikáty** vyberte **Přidat**.
2. Do pole **Název** zadejte název tajného kódu účtu úložiště. Zadejte popis do pole **Popis**.
3. V poli **Typ** vyberte **Certifikát**.
4. Zvolte **Uložit** a pak zavřete stránku.

## <a name="create-an-electronic-invoicing-add-on-environment"></a>Vytvoření prostředí doplňku elektronické fakturace

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Elektronická fakturace**.

## <a name="create-a-service-environment"></a>Vytvoření servisního prostředí

1. Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby**.
2. Vyberte **Nový** pro vytvoření nového prostředí služby.
3. Do pole **Název** zadejte název prostředí elektronické fakturace. Zadejte popis do pole **Popis**.
4. V poli **Tajný klíč tokenu SAS úložiště** vyberte název certifikátu, který se musí použít k ověření přístupu k účtu úložiště.
5. V části **Uživatelé** vyberte **Přidat**, chcete-li přidat uživatele, který má povoleno odesílat elektronické faktury prostřednictvím prostředí a také se připojit k účtu úložiště.
6. Do pole **ID uživatele** zadejte alias uživatele. Do pole **E-mail** zadejte e-mailovou adresu uživatele.
7. Zvolte **Uložit**.
8. Pokud faktury pro vaši zemi/region vyžadují pro použití digitálních podpisů řetězec certifikátů, v podokně akcí vyberte **Parametry Key Vault** a poté zadejte **Sekvence certifikátů** a postupujte následovně:

    1. Vyberte **Nový** k vytvoření sekvence certifikátů.
    2. Do pole **Název** zadejte název sekvence certifikátů. Zadejte popis do pole **Popis**.
    3. V části **Certifikáty** vyberte **Přidat**, abyste přidali certifikát do sekvence.
    4. Pomocí tlačítek **Nahoru** a **Dolů** změňte polohu certifikátu v řetězci.
    5. Zvolte **Uložit** a pak zavřete stránku.
    6. Zavřete stránku.
9. Na stránce **Prostředí služby** v podokně akcí vyberte **Publikovat**, chcete-li publikovat prostředí do cloudu. Hodnota pole **Stav** se změní na **Publikováno**.

## <a name="create-a-connected-application"></a>Vytvoření propojené aplikace

1. Na stránce **Nastavení prostředí** v podokně akcí vyberte **Propojené aplikace**.
2. Zvolte **Nový** pro vytvoření propojené aplikace.
3. Do pole **Název** zadejte název aplikace, ke které se má provést připojení.
4. Do pole **Aplikace** zadejte adresu URL prostředí Finance and Supply Chain Management pro připojení.
4. Do pole **Klient** zadejte klienta prostředí Finance and Supply Chain Management.
5. Zvolte **Uložit**.
6. V podokně akcí vyberte **Zkontrolovat připojení**, abyste otestovali spojení s prostředím. Poté stránku zavřete.

## <a name="link-connected-applications-to-environments"></a>Propojení připojených aplikace s prostředím

1. Na stránce **Nastavení prostředí** vyberte **Nový** a přiřaďte připojenou aplikaci prostředí.
2. V poli **Připojená aplikace** vyberte připojenou aplikaci.
3. V poli **Prostředí služby** vyberte prostředí služeb.
4. Zvolte **Uložit** a pak zavřete stránku.

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>Nastavte integraci doplňku elektronické fakturace ve Finance a Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Zapněte funkci integrace doplňku elektronické fakturace

1. Přihlaste se k instanci Finance nebo Supply Chain Management.
2. V pracovním prostoru **Správa funkcí** vyhledejte funkci **Integrace doplňku elektronické fakturace**. Pokud se tato funkce na stránce neobjeví, vyberte **Zkontrolovat aktualizace**.
3. Vyberte funkci a poté vyberte tlačítko **Povolit nyní**.

### <a name="set-up-the-service-endpoint-url"></a>Nastavte adresu URL koncového bodu služby

1. Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.
2. Na kartě **Služba odeslání** v poli **Identifikátor URL koncového bodu služby** zadejte příslušný koncový bod služby pro vaši geografii Azure, jak je znázorněno v následující tabulce.

    | Geografie datového centra Azure | URL adresa koncového bodu služby                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Východní USA                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | USA – západ                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Sever EU                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Západ EU                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. Do pole **Prostředí** zadejte název prostředí doplňku elektronické fakturace.
4. Zvolte **Uložit** a pak zavřete stránku.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]