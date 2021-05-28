---
title: Začínáme se správou služby Elektronické fakturace
description: Toto téma poskytuje informace, jak začít s Elektronickou fakturací.
author: gionoder
ms.date: 05/04/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f389e111006327fe8d82581d01140b4cff2e200d
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980968"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Začínáme se správou služby Elektronické fakturace

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Předpoklady

Než provedete postupy v tomto tématu, musí být splněny následující předpoklady:

- Musíte mít přístup ke svému účtu Microsoft Dynamics Lifecycle Services (LCS).
- Musíte mít projekt LCS, který obsahuje verzi 10.0.17 nebo novější nástroje Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management. Kromě toho musí být tyto aplikace nasazeny v jedné z následujících geografických oblastí Azure:

    - Spojené státy americké
    - Evropa
    - Spojené království
    - Asie

- Musíte mít přístup ke svému účtu Dynamics 365 Regulatory Configuration Services (RCS).
- Musíte aktivovat funkci Globalizace pro svůj účet RCS v modulu Správa funkcí. Pro více informací viz [Regulatory Configuration Services (RCS) - funkce globalizace](rcs-globalization-feature.md).
- Musíte vytvořit trezor klíčů a účet úložiště Azure. Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Nainstalujte doplněk pro mikroslužby ve službě Lifecycle Services

1. Přihlaste se k účtu LCS.
2. Vyberte dlaždici **Náhled správy funkcí**.
3. V části **Funkce Public Preview** vyberte **Elektronická fakturace**.
4. Ujistěte se, zda je možnost **Funkce Preview zapnuta** nastavena na hodnotu **Ano**.
5. Na řídicím panelu projektu LCS vyberte svůj projekt nasazení LCS.
6. V projektu LCS vyberte na řídicím panelu prostředí LCS svůj projekt nasazení LCS. Projekt nasazení LCS musí být spuštěný.
7. Na kartě **Integrace Power Platform** ve skupině polí **Doplňky prostředí** vyberte **Instalovat nový doplněk**.
8. Vyberte **Nastavení elektronické fakturace**.
9. V poli **ID aplikace AAD** zadejte **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Toto je pevná hodnota.
10. V poli **ID klienta AAD** zadejte ID tenanta účtu předplatného Azure.
11. Zkontrolujte smluvní podmínky a poté zaškrtněte políčko.
12. Vyberte **Instalovat**.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Nastavení parametrů pro integraci RCS s Elektronickou fakturací

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Elektronické výkaznictví** v části **Související odkazy** vyberte **Parametry elektronického výkaznictví**.
3. Na kartě **Služba elektronické fakturace** v poli **Identifikátor URI koncového bodu služby** zadejte příslušný koncový bod služby pro vaši geografii Azure, jak je znázorněno v následující tabulce.

    | Geografie datového centra Azure | URI adresa koncového bodu služby                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Spojené státy americké              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Evropa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Spojené království             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asie                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. Ověřte, zda je pole **Id aplikace** nastaveno na **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Tato hodnota je pevná hodnota.
5. V poli **ID prostředí LCS** zadejte ID prostředí LCS.
6. Zvolte **Uložit** a pak zavřete stránku.

## <a name="create-key-vault-references"></a>Vytvoření referencí úložiště klíčů

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Elektronická fakturace**.
3. Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby** a potom vyberte **Parametry Key Vault**.
4. Vyberte možnost **Nová** k vytvoření reference trezoru klíčů.
5. Do pole **Název** zadejte název reference trezoru klíčů. Zadejte popis do pole **Popis**.
6. Do pole **URI trezoru klíčů** vložte tajný kód trezoru klíčů z Azure Key Vault. Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).
7. Zvolte **Uložit**.

## <a name="create-storage-account-secret"></a>Vytvoření tajného kódu účtu úložiště

1. Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby** >  **Parametry trezoru klíčů**.
2. Vyberte **Reference trezoru klíčů** a v části **Certifikáty** vyberte **Přidat**.
3. Do pole **Název** zadejte název tajného kódu účtu úložiště. Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).
4. Zadejte popis do pole **Popis**.
5. V poli **Typ** vyberte **Tajný klíč**.
6. Zvolte **Uložit** a pak zavřete stránku.

## <a name="create-a-digital-certificate-secret"></a>Vytvoření tajného klíče digitálního certifikátu

1. Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby** a potom vyberte **Parametry trezoru klíčů**.
2. Vyberte **Reference trezoru klíčů** a poté v části **Certifikáty** vyberte **Přidat**.
3. Do pole **Název** zadejte název tajného kódu digitálního certifikátu. Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).
4. Zadejte popis do pole **Popis**.
5. V poli **Typ** vyberte **Certifikát**.
6. Zvolte **Uložit** a pak zavřete stránku.

## <a name="create-a-service-environment"></a>Vytvoření servisního prostředí

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Elektronická fakturace**.
3. Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby**.
4. Vyberte **Nový** pro vytvoření nového prostředí služby.
5. Do pole **Název** zadejte název prostředí elektronické fakturace. Zadejte popis do pole **Popis**.
6. V poli **Tajný klíč tokenu SAS úložiště** vyberte název tajného klíče účtu úložiště, který se musí použít k ověření přístupu k účtu úložiště.
7. V části **Uživatelé** vyberte **Přidat**, chcete-li přidat uživatele, který má povoleno odesílat elektronické faktury prostřednictvím prostředí a také se připojit k účtu úložiště.
8. Do pole **ID uživatele** zadejte alias uživatele. Do pole **E-mail** zadejte e-mailovou adresu uživatele.
9. Zvolte **Uložit**.
10. Pokud faktury pro vaši zemi/region vyžadují pro použití digitálních podpisů řetězec certifikátů, v podokně akcí vyberte **Parametry Key Vault** a poté zadejte **Sekvence certifikátů** a postupujte následovně:
    1. Vyberte **Nový** k vytvoření sekvence certifikátů.
    2. Do pole **Název** zadejte název sekvence certifikátů. Zadejte popis do pole **Popis**.
    3. V části **Certifikáty** vyberte **Přidat**, abyste přidali certifikát do sekvence.
    4. Pomocí tlačítek **Nahoru** a **Dolů** změňte polohu certifikátu v řetězci.
    5. Zvolte **Uložit** a pak zavřete stránku.
    6. Zavřete stránku.
11. Na stránce **Prostředí služby** v podokně akcí vyberte **Publikovat**, chcete-li publikovat prostředí do cloudu. Hodnota pole **Stav** se změní na **Publikováno**.

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

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Nastavte integraci doplňku elektronické fakturace ve Finance a Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>Zapněte funkci integrace Elektronické fakturace

1. Přihlaste se k instanci Finance nebo Supply Chain Management.
2. V pracovním prostoru **Správa funkcí** vyhledejte funkci **Integrace Elektronické fakturace**. Pokud se tato funkce na stránce neobjeví, vyberte **Zkontrolovat aktualizace**.
3. Vyberte funkci a poté vyberte tlačítko **Povolit nyní**.

### <a name="set-up-the-service-endpoint-url"></a>Nastavte adresu URL koncového bodu služby

1. Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.
2. Na kartě **Služba odeslání** v poli **Identifikátor URL koncového bodu služby** zadejte příslušný koncový bod služby pro vaši geografii Azure, jak je znázorněno v následující tabulce.

    | Geografie datového centra Azure | URI adresa koncového bodu služby                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Spojené státy americké              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Evropa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Spojené království             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asie                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Do pole **Prostředí** zadejte název prostředí služby, které je publikováno v Elektronické fakturaci.
4. Zvolte **Uložit** a pak zavřete stránku.

### <a name="enable-flighting-keys"></a>Povolit testovacích klíčů

Povolte testovací klíče pro Microsoft Dynamics 365 Finance nebo Microsoft Dynamics 365 Supply Chain Management verze 10.0.17 nebo starší. 
1. ProveĎte následující příkaz SQL:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Proveďte příkaz IISreset pro všechny AOS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
