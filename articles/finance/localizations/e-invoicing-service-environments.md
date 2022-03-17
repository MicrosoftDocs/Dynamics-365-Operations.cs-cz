---
title: Prostředí služby
description: Toto téma obsahuje informace o prostředích služeb pro elektronickou fakturaci a vysvětluje, jak je nastavit.
author: dkalyuzh
ms.date: 02/28/2022
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
ms.openlocfilehash: a8a135098f71e1413cd20ff8ad4003f090ae3407
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371568"
---
# <a name="service-environments"></a>Prostředí služby

[!include [banner](../includes/banner.md)]

Prostředí služeb jsou logické oddíly, které jsou vytvořeny na podporu provádění funkcí globalizace a odpovídajících dokumentů, které jsou zpracovávány ve službě Elektronické fakturace. Tajné klíče zabezpečení a digitální certifikáty a přístupová oprávnění (zásady správného řízení) musí být nakonfigurovány na úrovni prostředí služby.

Můžete vytvořit tolik prostředí služeb, kolik potřebujete. Všechna prostředí služeb, která vytvoříte, jsou na sobě navzájem nezávislá. Jako osvědčený postup doporučujeme vytvořit alespoň dvě prostředí služeb:

- Jedno prostředí pro hlavní účely vývoje a ověřování. Toto prostředí je obvykle prostředí uživatelského akceptačního testování (UAT).
- Jedno prostředí pro produkční účely. Toto prostředí je obvykle produkční prostředí.

Tento typ rozdělení pomáhá zajistit, aby byly procesy elektronické fakturace ověřeny a přizpůsobeny v izolovaném prostoru předtím, než jdou do produkce.

Prostředí služeb musí být vytvořeno a udržováno ve službě Regulatory Configuration Service (RCS). Pak když budete připraveni, musí být publikovány ve službě Elektronické fakturace. Publikační proces odesílá parametry prostředí služby z instance RCS do služby Elektronická fakturace.

Pokud neprovedete proces publikování poté, co vytvoříte nové prostředí služby nebo upravíte stávající prostředí služby (například přidáním nebo odebráním uživatelů nebo tajných klíčů Microsoft Azure Key Vault), změny nebudou účinné. Pro Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management jsou přístupná pouze publikovaná prostředí.

## <a name="service-environment-statuses"></a>Stavy prostředí služeb

Prostředí služeb lze spravovat prostřednictvím jejich stavu. Stav prostředí můžete zobrazit na stránce **Prostředí služeb**. K dispozici jsou následující stavy:

- **Nepublikováno** – Prostředí bylo vytvořeno, ale dosud nebylo publikováno.
- **Publikováno** – Prostředí bylo publikováno v doplňku služby elektronické fakturace.
- **Změněno** – Atributy publikovaného prostředí byly změněny, ale změny ještě nebyly publikovány.

## <a name="users"></a>Uživatelé

Každé prostředí služeb musí obsahovat seznam uživatelů, kteří se mohou připojit k elektronické fakturaci z Finance nebo Supply Chain Management.

## <a name="applications"></a>Žádosti

V některých scénářích se mohou ke službě elektronické fakturace připojit jiné aplikace než Finance nebo Supply Chain Management, aby mohly odeslat elektronické dokumenty k dalšímu zpracování nebo získat informace, jako je stav odeslání dokumentu. V těchto scénářích by měla být aplikace definována v seznamu aplikací. Získá tak přístup ke službě Elektronická fakturace. Aplikace musí být také registrována jako aplikace v Azure Active Directory (Azure AD) a k její identifikaci je nutné použít ID objektu. 

Protože společnost Microsoft vyžaduje vysokou úroveň kontroly zabezpečení aplikací, které se mohou připojit ke službě elektronické fakturace, musíte kontaktovat společnost Microsoft na <DGXRegulatoryservicesengineering@service.microsoft.com> a uvést následující údaje o své aplikaci:

- ID klienta Azure AD
- ID prostředí Microsoft Dynamics Lifecycle Services (LCS)
- ID aplikace (ID klienta)
- ID objektu
- Odůvodnění a podrobný popis žádosti

Společnost Microsoft žádost vyhodnotí a zaregistruje aplikaci v registru zabezpečení, aby bylo zajištěno, že může fungovat s elektronickou fakturací.

## <a name="number-sequences"></a>Číselné řady

Pokud vaše scénáře vyžadují číselné řady (například v názvech souborů), můžete použít číselné řady, které jsou definovány pro konkrétní prostředí, ale které lze použít buď napříč funkcemi globalizace, nebo pro konkrétní funkci globalizace. Po definování číselné řady ji můžete použít v proměnných a procesních kanálech. Chcete-li sledovat jeho použití, na stránce **Číselné řady** vyhledejte hodnotu **Aktuální** pro parametr **Používá se**.

### <a name="working-with-number-sequences"></a>Práce s číselnými řadami
Na stránce **Číselné řady**: 

- Zvolte **Nový** pro vytvoření číselné řady. Poté zadejte název a popis. 
- Vyberte **Odstranit** pro smazání číselné řady, pokud se již nepoužívá.
- Nemusíte vybírat **Publikovat** v podokně akcí pro publikování změny číselné řady. Aktualizace se provádí automaticky.

## <a name="create-a-key-vault-reference"></a>Vytvoření reference trezoru klíčů

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Elektronická fakturace**.
3. Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby**.
4. Na stránce **Prostředí služby** v podokně akcí vyberte Prostředí služby **Parametry trezoru klíčů**.
5. Na stránce **Parametry úložiště klíčů** vyberte **Nový** a vytvořte referenci trezoru klíčů.
6. Do pole **Název** zadejte název reference trezoru klíčů.
7. Zadejte popis do pole **Popis**.
8. Do pole **URI trezoru klíčů** vložte URI trezoru klíčů z trezoru klíčů (`https://<your key vault>.vault.azure.net/`). Další informace viz [Vytvoření Azure key vault na portálu Azure](e-invoicing-create-azure-key-vault-azure-portal.md).
9. Zvolte možnost **Uložit**.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Vytvoření tajného klíče pro tajný token účtu úložiště

1. Na stránce **Parametry trezoru klíčů** vyberte referenci trezoru klíčů, kterou jste vytvořili v předchozím postupu, a poté v části **Certifikáty** vyberte **Přidat**.
2. Do pole **Název** zadejte název tajného kódu účtu úložiště. Tento název by se měl shodovat s názvem tajného klíče trezoru klíčů, který obsahuje token sdíleného přístupového podpisu úložiště (SAS). Další informace viz [Vytvoření účtu úložiště Azure na portálu Azure](e-invoicing-create-azure-storage-account-azure-portal.md). 
3. Zadejte popis do pole **Popis**.
4. V poli **Typ** vyberte **Tajný klíč**.
5. Zvolte možnost **Uložit**.
    
## <a name="create-a-service-environment"></a>Vytvoření servisního prostředí

1. Na stránce **Prostředí služeb** v podokně akcí vyberte **Nové** k vytvoření prostředí služeb.
2. Do pole **Název** zadejte název prostředí elektronické fakturace.
3. Zadejte popis do pole **Popis**.
4. V poli **Tajný klíč tokenu SAS úložiště** vyberte název tajného klíče účtu úložiště, který se musí použít k ověření přístupu k účtu úložiště.
5. V části **Uživatelé** vyberte **Přidat**, chcete-li přidat uživatele, který má povoleno odesílat elektronické faktury prostřednictvím prostředí a připojit se k účtu úložiště.
6. Do pole **ID uživatele** zadejte alias uživatele. 
7. Do pole **E-mail** zadejte e-mailovou adresu uživatele.
8. Zvolte možnost **Uložit**.
9. V podokně akcí vyberte **Publikovat**, chcete-li publikovat prostředí do služby elektronické fakturace. Ověřte, že hodnota pole **Stav** se změní na **Publikováno**.
