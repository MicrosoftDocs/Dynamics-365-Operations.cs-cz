---
title: Zákaznické certifikáty a tajné kódy
description: Toto téma poskytuje informace o nastavení certifikátů a tajných kódů v Elektronické fakturaci.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1325cad95e9a6dc470691f5f168439fccaaa78e1
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371579"
---
# <a name="customer-certificates-and-secrets"></a>Zákaznické certifikáty a tajné kódy

[!include [banner](../includes/banner.md)]

Pokud již máte referenci Key Vault Microsoft Azure ve službě Regulatory Configuration Service (RCS), můžete vytvořit reference na certifikáty a tajné kódy Key Vault. Pokud ještě nemáte referenci Key Vault, informace o jejím vytvoření najdete v tématu [Prostředí služeb](e-invoicing-service-environments.md).

## <a name="create-certificates-and-secrets"></a>Vytvoření certifikátů a tajných kódů

Chcete-li vytvořit a nastavit certifikáty a tajné kódy, postupujte podle těchto kroků.

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Elektronická fakturace**.
3. Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby**.
4. Na stránce **Prostředí služby** v podokně akcí vyberte Prostředí služby **Parametry trezoru klíčů**.
5. Na stránce **Parametry Key Vault** vyberte referenci Key Vault a poté v části **Certifikáty** vyberte **Přidat**.
6. Do pole **Název** zadejte název certifikátu nebo tajného kódu Key Vault. Další informace viz [Vytvoření účtu úložiště Azure na portálu Azure](e-invoicing-create-azure-storage-account-azure-portal.md).
7. Zadejte popis do pole **Popis**.
8. V poli **Typ** vyberte **Certifikát** pokud odkazujete na certifikát, který je uložen v trezoru klíčů. Vyberte možnost **Tajný**, pokud odkazujete na tajný kód, který je uložen v trezoru klíčů.
9. Zvolte možnost **Uložit**.

> [!NOTE]
> V některých scénářích musíte použít veřejné certifikáty s příponou názvu souboru .cer. Key Vault však nepodporuje import a ukládání certifikátů tohoto typu jako certifikátů Key Vault. V těchto scénářích byste měli uložit soubor .cer jako řetězec X.509 (.CER) kódovaný algoritmem Base-64. Poté do tajného kódu Key Vault uložte řetězec, který je v souboru mezi řádkem **BEGIN CERTIFICATE** a řádkem **END CERTIFICATE**. V prostředí služby byste přesto měli vytvořit referenci na záznam Key Vault a nastavit pole **Typ** na **Osvědčení**.

## <a name="create-a-chain-of-certificates"></a>Vytvoření řetězce certifikátů

Pokud vaše faktury pro konkrétní zemi/oblast vyžadují řetězec certifikátů k použití digitálních podpisů nebo vytvoření zabezpečeného (Secure Sockets Layer \[SSL\]) připojení k externím webovým službám, vytvořte řetězec certifikátů, ve kterém jsou certifikáty v následujícím pořadí:

1. Kořenové certifikáty
2. Zprostředkující certifikáty
3. Certifikáty koncových uživatelů

Kořenové certifikační autority (CA) jsou důvěryhodným zdrojem certifikátů. Certifikáty zprostředkujících CA jsou mosty, které propojují certifikáty koncových uživatelů s certifikáty kořenové autority.

Chcete-li vytvořit a nastavit řetězec certifikátů, postupujte podle těchto kroků.

1. Na stránce **Parametry Key Vault** v podokně akcí vyberte **Řetězec certifikátů**.
2. Vyberte **Nový** k vytvoření sekvence certifikátů.
3. Do pole **Název** zadejte název řetězce certifikátů.
4. Zadejte popis do pole **Popis**.
5. V části **Certifikáty** vyberte **Přidat**, abyste přidali certifikát do sekvence.
6. Pomocí tlačítek **Nahoru** a **Dolů** změňte polohu certifikátu v řetězci. Kořenový certifikát CA ponechte nahoře na začátku seznamu a certifikát koncového uživatele na konci.
7. Zvolte možnost **Uložit**.

Ve službě RCS můžete vytvořit tolik referencí Key Vault, kolik chcete. Pamatujte, že tajný kód pro token sdíleného přístupového podpisu úložiště (SAS) se používá k propojení daného prostředí služby s referencí Key Vault. Můžete odkazovat na certifikáty a tajné kódy Key Vault, které jsou uloženy v trezoru klíčů, který také obsahuje tajný kód pro token úložiště SAS, které používáte při nastavování prostředí služby.
