---
title: Poradce při potížích se synchronizací v ostrém provozu
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy se synchronizací v ostrém provozu.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a0a14c87af7f0d2372d752233f21d9accbca58a8
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542508"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Poradce při potížích se synchronizací v ostrém provozu

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse. Toto téma obsahuje informace, které vám pomohou vyřešit problémy se synchronizací v ostrém provozu.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Synchronizace v ostrém provozu vyvolá chybu 403 Forbidden při vytváření řádku v aplikaci Finance and Operations

Může se zobrazit následující chybová zpráva při vytváření řádku v aplikaci Finance and Operations:

*\[{\\"chyba\\":{\\"kód\\":\\"0x80072560\\",\\"zpráva\\":\\"Uživatel není členem organizace.\\"}}\], Vzdálený server vrátil chybu: (403) zakázáno."}}".*

Chcete-li tento problém vyřešit, postupujte podle kroků v [Požadavcích na systém a jeho předpoklady](requirements-and-prerequisites.md). K provedení těchto kroků musí mít uživatelé aplikace se dvojím zápisem, kteří jsou vytvořeni v aplikaci Dataverse, roli správce systému. Výchozí vlastnící tým musí mít také roli správce systému.

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Synchronizace v ostrém provozu pro libovolnou tabulku neustále vyvolává podobnou chybu při vytváření řádku v aplikaci Finance and Operations.

**Požadovaná role pro opravu problému:** správce systému

Při každém pokusu o uložení dat tabulky do aplikace Finance and Operations se může zobrazit chybová zpráva podobná následující:

*Nelze uložit změny do databáze. Jednotka práce nemůže potvrdit transakci. Nelze zapsat data do entity uoms. Zápisy do UnitOfMeasureEntity se nezdařily. Chybová zpráva Nelze synchronizovat s entitou uoms.*

Chcete-li tento problém vyřešit, je nutné zajistit, aby v aplikaci Finance and Operations i Dataverse existovala potřebná referenční data. Pokud například zákazník, který je součástí aplikace Finance and Operations, patří do určité skupiny odběratelů, ujistěte se, že v Dataverse existuje daná skupina odběratelů.

Pokud existují data na obou stranách a potvrdili jste, že problém není související s daty, postupujte následujícím způsobem.

1. Zastavte související tabulku.
2. Přihlaste se k aplikaci Finance and Operations a ujistěte se, že v tabulce DualWriteProjectConfiguration a DualWriteProjectFieldConfiguration existují řádky pro nefunkční entitu. Takto například dotaz vypadá, pokud tabulka **Zákazníci** selhává.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Pokud existují řádky pro neúspěšnou tabulku i po zastavení mapování tabulek, odstraňte řádky, které souvisejí s chybnou tabulkou. Poznamenejte si sloupec **ProjectName** v tabulce DualWriteProjectConfiguration a načtěte řádek v tabulce DualWriteProjectFieldConfiguration použitím názvu projektu k odstranění řádku.
4. Spusťte mapování tabulek. Ověřte, zda se data synchronizují bez problémů.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Zpracování chyb oprávnění ke čtení nebo zapisování při vytváření dat v aplikaci Finance and Operations

Při vytváření dat v aplikaci Finance and Operations se může zobrazit chybová zpráva "špatný požadavek", která se podobá následujícímu příkladu.

![Příklad chybové zprávy o chybném požadavku.](media/error_record_id_source.png)

Chcete-li tento problém vyřešit, je nutné přiřadit správné roli zabezpečení týmu mapované obchodní jednotky Dynamics 365 Sales nebo Dynamics 365 Customer Service, aby bylo možné chybějící oprávnění povolit.

1. V aplikaci Finance and Operations vyhledejte organizační jednotku, která je mapována v sadě Data Integration Connection.

    ![Mapování organizace.](media/mapped_business_unit.png)

2. Přihlaste se k prostředí v aplikaci customer engagement, přejděte k **Nastavení \> Zabezpečení** a najděte tým mapované organizační jednotky.

    ![Tým mapované organizační jednotky.](media/setting_security_page.png)

3. Otevřete stránku pro tým pro úpravy a poté výběrem možnosti **Spravovat role** otevřete dialogové okno **Spravovat role týmu**.

    ![Tlačítko Spravovat role.](media/manage_team_roles.png)

4. Přiřaďte roli, která má oprávnění pro čtení a zápis pro příslušné tabulky, a pak vyberte **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Oprava synchronizačních potíží v prostředí, které má nedávno změněné prostředí Dataverse

**Požadovaná role pro opravu problému:** správce systému

Může se zobrazit následující chybová zpráva při vytváření dat v aplikaci Finance and Operations:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Nelze generovat datovou část pro entitu CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Vytvoření zatížení se nezdařilo s chybou Neplatný identifikátor URI: Identifikátor URI je prázdný."}\],"isErrorCountUpdated":true}*

Takto vypadá chyba v aplikaci customer engagement:

*V kódu ISV došlo k neočekávané chybě. (ErrorType = ClientError) Neočekávaná výjimka z modulu plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: Nepodařilo se zpracovat účet entity. (Pokus o připojení se nezdařil, protože připojená strana nereagovala správně po určitém časovém období, nebo navázané připojení se nezdařilo, protože připojený hostitel neodpověděl.)*

K této chybě dojde, pokud je prostředí Dataverse nesprávně resetováno v okamžiku, kdy se pokusíte vytvořit data v aplikaci Finance and Operations.

Chcete-li opravit problém, postupujte následovně.

1. Přihlaste se k virtuálnímu počítači (VM) Finance and Operations, otevřete SQL Server Management Studio (SSMS) a hledejte řádky v tabulce DUALWRITEPROJECTCONFIGURATIONENTITY, kde **internalentityname** rovná se **Zákazníci V3** a **externalentityname** rovná se **účty**. V tomto poli je uveden vzhled dotazu.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. Chcete-li spustit následující dotaz, použijte název projektu z výsledků předchozího dotazu.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. Zkontrolujte, zda má sloupec **externalenvironmentURL** správnou Dataverse adresu URL aplikace. Odstraňte všechny duplicitní řádky, které ukazují na nesprávnou adresu URL Dataverse. Odstraňte odpovídající řádky z tabulek DUALWRITEPROJECTFIELDCONFIGURATION a DUALWRITEPROJECTCONFIGURATION.
4. Zastavte mapování tabulek a restartujte jej

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
