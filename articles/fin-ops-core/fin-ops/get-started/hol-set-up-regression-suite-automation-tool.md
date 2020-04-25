---
title: Nastavení a instalace kurzu pro nástroj Regression Suite Automation Tool
description: Toto téma je kurz, který ukazuje, jak nastavit a nainstalovat nástroj Regression suite automation tool (RSAT).
author: robinarh
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: f5670f6a580249491ad16ae46470160545bb8f91
ms.sourcegitcommit: 4fdee254649a751d46632fb4d0d48698e112fa72
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248706"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Nastavení a instalace kurzu pro nástroj Regression Suite Automation Tool
Toto téma je kurz, který vám pomůže získat instalační program a začít s nástrojem RSAT a nástroji spojenými s používáním nástroje RSAT. 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Pomocí nástrojů internetového prohlížeče můžete tuto stránku stáhnout a uložit ve formátu PDF. 

## <a name="key-concepts"></a>Klíčové koncepty

- Vysvětlení instalace a nezbytných nastavení vyžadovaných pro různé aplikace podporující nástroj Regression Suite Automation Tool (RSAT).
- Vysvětlení, jak funkce Záznamník úloh spolu s funkcí Microsoft Dynamics Lifecycle Services (LCS) a Microsoft Azure DevOps umožňují vytvářet, konfigurovat, spouštět, zkoumat a vykazovat testovací případy.
- Pomocí záznamníku úkolů můžete funkčním uživatelům umožnit záznam obchodních úkolů a poté převést záznamy úkolů na sadu automatizovaných testů, aniž by bylo nutné vytvářet zdrojový kód.

## <a name="before-you-begin"></a>Než začnete

### <a name="prerequisites"></a>Předpoklady

- V tomto kurzu je vyžadováno prostředí s aplikací Microsoft Dynamics 365 for Finance and Operations verze 10.0 (duben 2019) nebo novější. Pro zákazníky, kteří používají Microsoft Dynamics 365 for Finance and Operations Enterprise edition 7.3, je podporována také Platform update 20 (PU20) nebo vyšší.
- Uživatel musí mít pro toto prostředí oprávnění správce.
- Musíte mít přístup do LCS tenanta zákazníka a Azure DevOps (dříve známé jako Microsoft Visual Studio Team Services \[VSTS\]).
- Uživatel, který vytváří a spravuje testy, musí mí licenci Azure DevOps Test Plans nebo Test Manager. Následující licence také umožní přístup k testovacím plánům:
    - Visual Studio Enterprise
    - Visual Studio Test Professional
    - Licence pro předplatitele Platforem MSDN
- Nástroje RSAT musí mít přístup k testovacímu prostředí prostřednictvím webového prohlížeče.
- Chcete-li vygenerovat a upravit parametry testu, musíte mít nainstalovánu aplikaci Microsoft Excel.

## <a name="configure-azure-devops"></a>Konfigurace služby Azure DevOps

### <a name="user-eligibility"></a>Způsobilost uživatele

Zkontrolujte, zda je uživatel vytvořen v aplikaci Azure DevOps a zda má úroveň předplatného, která poskytuje přístup k plánům testování Azure. Licence Azure DevOps Test Plans je vyžadována pouze v případě, že uživatel vytvoří a spravuje testovací případy (tj. ne všichni uživatelé RSAT musí tuto licenci vlastnit). Informace o licenčních požadavcích naleznete v tématu [Licenční požadavky](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).

### <a name="create-a-new-azure-devops-project"></a>Vytvoření nového projektu Azure DevOps
RSAT využívá Azure DevOps pro účely testování a správy testovacích sad, vytváření sestav a zkoumání výsledků testovacího běhu. 

> [!NOTE]
> Můžete použít existující projekt Azure DevOps. Pokud je však existující projekt Azure DevOps nastaven tak, že má vlastní šablonu, obdržíte při synchronizaci testovacích případů z modulu Modelování podnikových procesů (BPM) do Azure DevOps chybu synchronizace VSTS (viz část [testování synchronizace z BPM do Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)). Pokud byly pro vlastní šablonu použity následující doporučené postupy, můžete testovací případy synchronizovat do Azure DevOps. (Tyto doporučené postupy jsou uvedeny v chybové zprávě.)

- Neodstraňujte žádné typy pracovních položek nebo integrovaná pole.
- Neodstraňujte žádný stav typu pracovních položek.
- Nepřidávejte žádná požadovaná pole k typu pracovních položek.

![Chybová zpráva se seznamem doporučených postupů](./media/setup_rsa_tool_02.png)

V opačném případě doporučujeme vytvořit nový projekt Azure DevOps. Další informace naleznete v tématu [Problematika synchronizace s BPM pomocí vlastní šablony procesu Azure DevOps](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/) (VSTS).

1. Otevřete Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).
2. Vyberte **Vytvořit projekt** v pravém horním rohu stránky Azure DevOps.

    ![Tlačítko Vytvořit projekt](./media/setup_rsa_tool_03.png)

3. Vyplňte následující pole a poté vyberte možnost **Vytvořit**:

    - **Název projektu**
    - **Kontrola verzí** – Vyberte **Kontrola verzí Team Foundation**. Všimněte si, že výchozí možnost **Git**není podporována.
    - **Proces položky práce**

    ![Dialogové okno Vytvořit nový projekt](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>Vytvoření osobního přístupového tokenu

V tomto kurzu budete používat Modelování podnikových procesů (BPM) k vytvoření testovacích případů a synchronizaci testovacích případů pomocí Azure DevOps. Chcete-li synchronizovat BPM s Azure DevOps, budete potřebovat osobní přístupový token.

1. Vyberte ikonu profilu v pravém horním rohu stránky pro váš projekt Azure DevOps a pak vyberte **zabezpečení**.

    ![Příkaz Zabezpečení](./media/setup_rsa_tool_05.png)

2. V levém podokně v části **Zabezpečení** vyberte možnost **Osobní přístupové tokeny**. Poté vyberte možnost **Nový token**.

    ![Tlačítko Nový token na kartě Osobní přístupové tokeny v uživatelském nastavení](./media/setup_rsa_tool_06.png)

3. Vyplňte následující pole a poté vyberte možnost **Vytvořit**:

    - **Název**
    - **Vypršení platnosti (UTC)** – vyberte **vlastní definovaný** a poté použijte výběr data k výběru posledního dostupného data.
    - **Rozsahy** – vyberte **úplný přístup**.

    ![Vytvoření dialogového okna Nový token pro osobní přístup](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > Poznamenejte si vytvořený osobní přístupový token. Budete jeh potřebovat později při nastavení konfigurace RSAT.

    ![Osobní přístupový token](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>Konfigurace projektu LCS

Pro vaši hlavní testovací knihovnu potřebujete projekt služby Lifecycle Services (LCS). Jako hlavní knihovnu pro testovací případy se používá služba Modelování podnikových procesů (BPM). BPM slouží ke správě a distribuci testovacích knihoven v rámci projektů LCS. Testovací případy ve formě kihoven BPM vydává například partner společnosti Microsoft nebo nezávislý dodavatel softwaru (ISV). V BPM jsou testovací případy uspořádány podle obchodního procesu. V BPM není definována objednávka nebo frekvence provádění testovacího průchodu. Tyto detaily jsou spravovány v Azure DevOps, jak je popsáno dále v tomto tématu.  

Pro svůj projekt LCS můžete použít existující zákaznickou implementaci nebo projekt partnera.

### <a name="update-the-lcs-language"></a>Aktualizace jazyka LCS

> [!NOTE]
> Chcete-li v uživatelském rozhraní správně zobrazit obchodní procesy, je nutné nastavit upřednostňovaný jazyk LCS na **Angličtina (Spojené státy)**.

1. Přejděte na projekt implementace LCS.
2. Zvolte tlačítko **Nastavení** tlačítko (symbol ozubeného kola) v pravém horním rohu stránky a vyberte **Jazyková předvolba**.

    ![Příkazy v nabídce nastavení](./media/setup_rsa_tool_09.png)

3. V poli **upřednostňovaný jazyk** vyberte **Angličtina (USA)** a pak vyberte možnost **Uložit**.

    ![Karta Jazykové předvolby v nastavení uživatele](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>Konfigurace LCS pro připojení k projektu Azure DevOps

Pokud jste dříve vytvořili nový projekt Azure DevOps, nakonfigurujte pro připojení k němu projekt LCS. Jinak, pokud je projekt LCS již připojen k projektu Azure DevOps, můžete přejít k následující části.

1. Přejděte na projekt implementace LCS.
2. Vyberte tlačítko **Nabídka** a poté vyberte **nastavení projektu**.

    ![Příkaz Nastavení projektu](./media/setup_rsa_tool_11.png)

3. V levém podokně vyberte **Visual Studio Team Services** a pak vyberte možnost **Nastavit Visual Studio Team Services**.

    ![Nastavení karty Visual Studio Team Services](./media/setup_rsa_tool_12.png)

4. V poli Adresa URL **Azure DevOps** zadejte adresu URL webu Azure DevOps. V poli **Osobní přístupový token** zadejte osobní přístupový token, který byl vytvořen dříve.

    > [!NOTE]
    > Ačkoli VSTS je nyní znám jako Azure DevOps, chcete-li připojit LCS Azure DevOps k projektu, použijte starou adresu URL. Například Azure DevOps URL používaná v tomto kurzu je `https://dev.azure.com/D365FOFastTrack/`. Na následujícím obrázku je však zadána možnost `https://D365FOFastTrack.visualstudio.com/`.

    ![Krok 1 v nastavení služby Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. Vyberte **Pokračovat**.
6. V poli Projekt **Visual Studio Team Services** vyberte projekt VST na vybraném webu pro odkazování na projekt LCS. Pole **Šablona procesu** je nastaveno ve výchozím nastavení na **Agilní**. Pro vlastní šablonu si prohlédněte doporučené postupy v oddílu [Vytvoření nového projektu Azure DevOps](#create-a-new-azure-devops-project) Pak vyberte **Pokračovat**.

    ![Krok 2 v nastavení služby Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. Zkontrolujte nastavení a pak vyberte možnost **Uložit**.

    ![Krok 3 v nastavení služby Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. Výběrem možnosti **Autorizovat** udělte skupině LCS přístup ke konfigurovanému webu Azure DevOps a zapněte funkce, které lze integrovat s VSTS.

    ![Tlačítko Autorizovat](./media/setup_rsa_tool_16.png)

9. Zobrazí se pole se zprávou "Budete přesměrováni na externí web pro autorizaci služby LCS, aby se mohla za vás připojovat k Visual Studio Team Services. Pokračovat?" Vyberte **Ano**.

    ![Okno se zprávou](./media/setup_rsa_tool_17.png)

10. Zvolte **Přijmout**.

    ![Autorizace přístupu](./media/setup_rsa_tool_18.png)

11. Pokud jste oprávněni jako uživatel, uživatelské rozhraní by se mělo vrátit na stránku nastavení projektu LCS.

    ![Oprávněný uživatel](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>Vytvoření nové knihovny BPM

1. Přejděte na projekt implementace LCS.
2. Vyberte tlačítko **Nabídka** a poté vyberte **Modelování podnikových procesů**.

    ![Příkaz Modelování podnikových procesů](./media/setup_rsa_tool_20.png)

3. Vyberte **Nová knihovna**.

    ![Tlačítko Nová knihovna](./media/setup_rsa_tool_21.png)

4. Do pole **Název knihovny** zadejte název a pak vyberte možnost **vytvořit**. V tomto výukovém kurzu pojmenujte knihovnu BPM **RSAT**.

    ![Dialogové okno Vytvořit novou knihovnu](./media/setup_rsa_tool_22.png)

5. Otevřete novou **knihovnu BPM** RSAT.
6. Vyberte **příklad základního obchodního procesu** a poté na pravé straně vyberte **režim úprav**.

    ![Tlačítko Režim úprav](./media/setup_rsa_tool_23.png)

7. Změňte hodnotu v poli **Název** a v poli **Popis** na **Vytvořit produkt**. Pak vyberte **Uložit**.

    ![Pole Název a Popis](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>Prostředí

### <a name="version-requirement"></a>Požadavek na verzi

Je požadován test nebo prostředí sandbox, na kterém běží verze 10. Pro zákazníky, kteří používají verzi 7.3, je podporována také Platform update 20 nebo vyšší.

> [!NOTE]
> Nástroje RSAT musí mít přístup k vašemu testovacímu prostředí prostřednictvím webového prohlížeče.

### <a name="user-criteria"></a>Kritéria uživatele

Uživatel musí mít pro toto prostředí oprávnění správce.

### <a name="set-up-help-settings-to-connect-with-lcs"></a>Nastavení nápovědy pro připojení s LCS

Tento krok je nutný pro připojení s LCS, aby bylo možné ukládat záznamy úkolů do příslušné knihovny BPM v systému LCS prostřednictvím klienta.

1. Spusťte klienta.
2. Přejděte do nabídky **Správa systému \> Nastavení \> systémových parametrů**.
3. Na kartě **Nápověda** v poli konfigurace nápovědy služby **Lifecycle Services** vyberte příslušný projekt LCS (**RSAT** pro tento kurz).

    ![Pole konfigurace nápovědy služby Lifecycle Services na kartě Nápověda](./media/setup_rsa_tool_25.png)

    Knihovny BPM jsou vyplněny v příslušném projektu LCS.

4. Zvolte **Uložit**.
5. Chcete-li zobrazit aktualizovaný obsah nápovědy, bude pravděpodobně nutné aktualizovat prohlížeč.

    ![Oznámení o aktualizaci prohlížeče](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>Zaznamenání úkolů

> [!NOTE]
> Zkontrolujte, zda jsou všechny záznamy úkolů v hlavním řídicím panelu zahájeny. Jednotlivé nahrávky uchovávejte tak, aby byly krátké, a zaměřujte se na jeden obchodní úkol, jako je vytvoření prodejní objednávky.

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>Vytvoření záznamu o úkolu a jeho uložení do knihovny BPM

Vytvořte odpovídající záznam úkolu, který můžete připojit k jednoduchému obchodnímu procesu, který byl vytvořen v nové knihovně BPM.

1. Spusťte klienta.
2. V hlavním řídicím panelu vyberte tlačítko **Nastavení** (symbol ozubeného kola) a poté vyberte položku **Záznamník úloh**.

    ![Příkazy v nabídce nastavení](./media/setup_rsa_tool_27.png)

3. Vyberte **Vytvořit nahrávku**.

    ![Tlačítko Vytvořit nahrávku](./media/setup_rsa_tool_28.png)

4. Vyplňte pole **Název nahrávky** a **Popis nahrávky** a pak vyberte **Spustit**.

    ![Pole Název nahrávky a Popis nahrávky](./media/setup_rsa_tool_29.png)

5. Zaznamenejte kroky pro vytvoření produktu. Po dokončení ukončete záznam výběrem tlačítka **Zastavit**.

    ![Postup při vytváření produktu](./media/setup_rsa_tool_30.png)

6. Vyberte **Uložit ve službách Lifecycle Services**.

    ![Možnosti uložení](./media/setup_rsa_tool_31.png)

    Informace o knihovně jsou načítány z LCS.

    ![Indikátor pokroku](./media/setup_rsa_tool_32.png)

7. Vyberte knihovnu BPM pro přidružení k záznamu úlohy. V tomto kurzu vyberte knihovnu **RSAT** BPM, která byla vytvořena dříve, a vytvořte v ní obchodní proces **Vytvořit produkt**. Pak vyberte **OK**.

    ![Přidružení záznamu o úkolu ke knihovně BPM a obchodnímu procesu](./media/setup_rsa_tool_33.png)

    Zobrazí se zpráva Uložení do služeb Lifecycle Services proběhlo úspěšně.

    ![Zpráva o úspěšném uložení na LCS](./media/setup_rsa_tool_34.png)

8. Chcete-li záznam úkolu uložit místně a poté jej odeslat do seznamu BPM pomocí LCS, postupujte následujícím způsobem:

    1. Po dokončení záznamu vyberte možnost **Uložit do tohoto počítače**.

        ![Možnosti uložení](./media/setup_rsa_tool_35.png)

    2. V oznamovacím panelu prohlížeče vyberte **Uložit** nebo **Uložit jako** a uložte soubor do místního počítače.

        ![Oznamovací panel](./media/setup_rsa_tool_36.png)

    3. Přejděte do knihovny **BPM** pro RSAT a vyberte obchodní proces, do kterého chcete uložit záznam úloh.
    4. Na kartě **Přehled** vyberte možnost **odeslat**.

        ![Tlačítko Odeslat](./media/setup_rsa_tool_37.png)

    5. Vyberte **Procházet** a vyberte soubor .axtr, který jste uložili dříve. Poté vyberte **odeslat**.

        ![Výběr souboru .axtr k odeslání](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>Testování synchronizace z BPM do Azure DevOps

Nyní, když je záznam úkolu připojen k obchodnímu procesu, je nutné ověřit, že obchodní proces a přidružený záznam úkolu mohou být synchronizovány s Azure DevOps jako funkce a testovací případ (v uvedeném pořadí) pomocí funkce synchronizace VSTS na LCS.

> [!NOTE]
> Odpovídající typ pracovní položky, který je vytvořen v aplikaci Azure DevOps, se bude lišit v závislosti na šabloně procesu, kterou jste vybrali při konfiguraci projektu LCS pomocí modulu Azure DevOps, jak je popsáno v tématu [vytvoření nového projektu Azure DevOps](#create-a-new-azure-devops-project).

1. Přejděte do knihovny BPM a otevřete knihovnu **RSAT**, kterou jste vytvořili dříve.
2. Vyberte tlačítko se třemi tečkami (**...**) a vyberte **Synchronizace VSTS**.

    ![Příkaz synchronizace VSTS v nabídce se třemi tečkami](./media/setup_rsa_tool_39.png)

    Po dokončení synchronizace VSTS se na levé straně zobrazí karta **Požadavky** a bude obsahovat odpovídající pracovní položku Azure DevOps.

    > [!NOTE]
    > Pracovní položka vytvořená v aplikaci Azure DevOps bude mít jako předponu názvu název knihovny BPM.

    ![Karta Požadavky](./media/setup_rsa_tool_40.png)

3. Aktualizujte stránku.
4. Vyberte tlačítko se třemi tečkami (**...**). Zobrazí se další možnost, **Synchronizace testovacích případů.** Vyberte tuto možnost.

    ![Příkaz synchronizace VSTS v nabídce se třemi tečkami](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > Pokud možnost **Synchronizace testovacích případů** není k dispozici po aktualizaci stránky, přejděte na hlavní stránku pro BPM a vyberte možnost **Synchronizovat testovací případy** pro celou knihovnu. Tímto způsobem efektivně vynutíte synchronizaci pro celou knihovnu.
    > 
    > ![Výběr testovacích případů synchronizace pro celou knihovnu](./media/setup_rsa_tool_42.png)

    Po dokončení testovacích případů synchronizace je na kartě **požadavky** vytvořen nový testovací případ.

    ![Nový testovací případ na kartě požadavky](./media/setup_rsa_tool_43.png)

5. Přejděte k projektu Azure DevOps a vyberte **Vývěsky \> Pracovní položky**.

    ![Příkaz pracovní položky v části Vývěsky](./media/setup_rsa_tool_44.png)

6. Ověřte, zda existuje pracovní položka a testovací případ, který jste vytvořili prostřednictvím synchronizace BPM.

    ![Pracovní položka a testovací případ](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>Instalace a konfigurace RSAT

RSAT lze nainstalovat do libovolného počítače se systémem Windows 10, který se může připojit k prostředí pomocí webového prohlížeče (Internet Explorer nebo webu Google Chrome).

> [!NOTE]
> Před zahájením instalace nové verze nástroje doporučujeme předchozí verzi odinstalovat.

### <a name="install-an-authentication-certificate"></a>Instalace ověřovacího certifikátu

Chcete-li povolit ověřování, je nutné vygenerovat a nainstalovat certifikát do stejného počítače, ve kterém je spuštěna RSAT.

#### <a name="generate-a-certificate"></a>Generování certifikátu

1. Chcete-li vygenerovat soubor certifikátu, otevřete okno prostředí Microsoft Windows PowerShell jako správce a spusťte následující příkaz.

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. Otevřete Správce certifikátů zadáním **certlm. msc** v dialogovém okně **Spustit** a potvrďte, že je certifikát **Automatický certifikát testování D365** vytvořen v části **Osobní \>Certifikáty**.

    > [!NOTE]
    > Nezapomeňte zadat **Certlm. msc**, nikoli **certmgr. msc**, protože certifikáty jsou uloženy v místním počítači.

    ![Certifikát D365 automatického testování](./media/setup_rsa_tool_46.png)

3. Klikněte pravým tlačítkem na databázi a poté vyberte možnost **Kopírovat**.
4. Přejděte na **Důvěryhodné kořenové certifikační autority \>** Certifikáty.

    ![Složka certifikáty pod složkou důvěryhodné kořenové certifikační autority](./media/setup_rsa_tool_47.png)

5. Výběrem možnosti **vložit** v nabídce **Akce** zkopírujte certifikát do umístění **důvěryhodných kořenových certifikačních autorit**.

    ![Příkaz Vložit v nabídce Akce](./media/setup_rsa_tool_48.png)

6. Chcete-li získat kryptografický otisk nainstalovaného certifikátu, ale bez mezer nebo zvláštních znaků, otevřete okno prostředí Windows PowerShell jako správce a spusťte následující příkazy.

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > Uložte kryptografický otisk, protože jej budete potřebovat později při aktualizaci souborů WIF pro aplikační objektový server (AOS) a nastavení konfigurace RSAT.

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>Konfigurace počítače AOS tak, aby důvěřoval připojení

> [!NOTE]
> Pokud je prostředí prostředím úrovně 2 +, kryptografický otisk certifikátu musí být aktualizován v souboru WIF. config pro **všechny** počítače AOS pro dané prostředí.

1. Navažte spojení s protokolem RDP (Remote Desktop Protocol) k počítači se serverem AOS. Podrobné informace o přihlášení jsou k dispozici na stránce Podrobnosti prostředí v systému LCS.
2. Otevřete službu Microsoft Internet Information Services (IIS) a v seznamu webů vyhledejte **AOSService**.

    ![AOSService v seznamu webů](./media/setup_rsa_tool_49.png)

3. Klikněte pravým tlačítkem na **Prozkoumat** a otevřete složku **\<Drive\>: \\AosService\\WebRoot**. Vyhledejte soubor **wif. config**.

    ![Soubor wif. config ve složce WebRoot](./media/setup_rsa_tool_50.png)

4. Aktualizujte **soubor wif.config** přidáním nového záznamu autority pro váš certifikát a název úřadu, jak je uvedeno v následujícím příkladu.

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > Pokud více uživatelů používá stejnou aplikaci, musí každý uživatel generovat samostatné kryptografické otisky a každý z těchto kryptografických otisků musí být přidán v části **\<klíče\>**.

5. Pokud existuje více než jeden počítač se serverem AOS, zopakujte kroky 3 až 4 pro každý další počítač.

    > [!NOTE]
    > Na rozdíl od prostředí starší úrovně 2 jsou nová prostředí s vrstvou 2 nasazena se dvěma instancemi AOS.

6. Spusťte příkaz **iisreset** ve všech počítačích AOS.

    > [!NOTE]
    > Pokud nemáte oprávnění správce ke spuštění příkazu **iisreset** v počítači s úrovní 1, vyberte na stránce Podrobnosti prostředí v nabídce LCS možnost udržovat > restartovat služby.

#### <a name="tier-2-environment"></a>Prostředí vrstvy 2+

Pokud se používá vrstva 2 + (standardní prostředí sandbox pro příjem testů nebo vyšší) prostředí, ověřte nebo nastavte následující nastavení registru v počítači, ve kterém je nainstalována sada RSAT. Tento krok je požadován, protože pomáhá předcházet chybám ověřování a RSAT.

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>Instalace RSAT

1. Přejděte na <https://www.microsoft.com/download/details.aspx?id=57357> a vyberte **Stáhnout**.
2. Vyberte všechny soubory a pak vyberte možnost **Další**.

    ![Výběr všech souborů](./media/setup_rsa_tool_51.png)

3. Poklepáním na balíček MSI spusťte instalační program. Po dokončení instalace vyberte možnost **Dokončit**.

    ![Instalační soubor služby RSAT](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>Instalace ovladačů a prohlížeče Selenium

Ve starších verzích aplikace RSAT bylo nutné instalovat ovladač a prohlížeč Selenium. Již není nutné instalovat tyto ovladače, protože jsou instalovány automaticky.

1. Při prvním spuštění aplikace RSAT se zobrazí výzva k automatickému stažení a instalaci programu Selenium. Další informace naleznete v tématu[Konfigurace RSAT](#configure-rsat).
2. Před spuštěním testovacího případu budete vyzváni k automatickému stažení a instalaci ovladače prohlížeče, který odpovídá výchozímu prohlížeči, který je vybrán v konfiguraci nástroje RSAT. Další informace naleznete v části [Případy zavádění a spouštění testovacích případů](#load-and-run-test-cases).

## <a name="get-started-with-rsat"></a>Začínáme s aplikací RSAT

### <a name="create-a-test-plan-and-test-suites"></a>Vytvoření testovacího plánu a sad testů

1. Přejděte k projektu Azure DevOps a vyberte možnost **testovací plány**.

    ![Příkaz Testovací plány](./media/setup_rsa_tool_53.png)

2. Vyberte **Nový testovací plán**.

    ![Tlačítko Nový testovací plán](./media/setup_rsa_tool_54.png)

3. Zadejte hodnotu do pole **Název** a vyberte **Vytvořit**. V tomto výukovém kurzu pojmenujte testovací plán **Testovací plán testování RSAT**.

    ![Dialogové okno Nový testovací plán](./media/setup_rsa_tool_55.png)

4. Vyberte znak (**+**) a pak vyberte **Statická sada** k vytvoření statické sady v rámci nového testovacího plánu. Pojmenujte novou sadu **T01 – Make to Stock**.

    > [!NOTE]
    > Můžete také vytvořit sadu založenou na dotazech, pokud chcete, aby nové testovací případy z BPM byly automaticky vyžádány v sadě pro RSAT.

    ![Vytvoření statické sady](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>Připojení testovacích případů k testovacím sadám

1. Vyberte **Přidat existující** napravo pro přidání existujících testovacích případů do testovací sady.

    ![Tlačítko Přidat existující aktivitu](./media/setup_rsa_tool_57.png)

2. Na stránce **Přidat testovací případy do sady** vyberte možnost **spustit dotaz** a pak vyberte testovací případ, který má být přidán do sady testů. V tomto kurzu vyberte testovací případ **Vytvořit nový případ**. Poté vyberte možnost **Přidat testovací případy** v pravém dolním rohu stránky (toto tlačítko není zobrazeno na následujícím obrázku).

    ![Tlačítko Spustit dotaz](./media/setup_rsa_tool_58.png)

    Testovací případ se přidá do sady **T01-Make to Stock**.

    ![Testovací případ přidaný do sady testů](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>Konfigurovat frontu RSAT

1. Otevřete RSAT.

    ![Ikona RSAT](./media/setup_rsa_tool_60.png)

2. Zobrazí se varovná zpráva s informací: Regression Suite Automation Tool vyžaduje Selenium, chcete ji automaticky stáhnout a nainstalovat? Vyberte **Ano**.

    ![Zpráva s upozorněním](./media/setup_rsa_tool_61.png)

3. Vyberte tlačítko **Nastavení** (symbol ozubeného kola) v pravém horním rohu a potom v zobrazeném dialogovém okně vyplňte následující pole:

    - **Azure DevOps Url** – Zadejte adresu URL projektu Azure DevOps, například `https://yourAzureDevOpsUrlHere.visualStudio.com`.
    - **Přístupový token** – zadejte přístupový token, který umožňuje nástroji připojení k Azure DevOps. Použijte osobní přístupový token, který jste vytvořili dříve v tomto kurzu. Další informace naleznete v tématu [Ověření přístupu s osobními přístupovými tokeny](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).
    - **Název projektu** – vyberte název projektu Azure DevOps.
    - **Testovací plán** – vyberte testovací plán Azure DevOps, který obsahuje vaše testovací případy. Další informace naleznete v tématu [Vytvoření testovacích plánů a sad testů](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan). Po výběru testovacího plánu vyberte možnost **Testovat připojení** pro otestování připojení k aplikaci Azure DevOps.
    - **Název hostitele** – zadejte název hostitele testovacího prostředí, například **\<myaos\>. cloudax.dynamics.com.** Nezahrnujte předponu **https://** nebo **http://**.
    - **Název hostitele SOAP** – zadejte název hostitele SOAP pro testovací prostředí. Název hostitele SOAP se obvykle shoduje s názvem hostitele, ale má příponu **SOAP**. Zde je příklad: **\<myaos\>soap.cloudax.dynamics.com**. Nezahrnujte předponu **https://** nebo **http://**.

        > [!NOTE]
        > Chcete-li najít název hostitele a název hostitele SOAP, spusťte Správce služby IIS, klikněte pravým tlačítkem na **Weby \> AOSService** a pak vyberte **Upravit vazby**. Hodnoty ve sloupci **Název hostitele** poskytují název hostitele a název hostitele SOAP (název hostitele SOAP má v adrese URL příponu **soap**).

        ![Název hostitele a název hostitele SOAP ve sloupci Název hostitele](./media/setup_rsa_tool_63.png)

    - **Uživatelské jméno správce** – zadejte e-mailovou adresu uživatele správce v testovacím prostředí.
    - **Kryptografický otisk** – zadejte kryptografický otisk ověřovacího certifikátu, jak je popsáno výše v tomto výukovém kurzu.
    - **Pracovní adresář** – zadejte umístění složky pro ukládání souborů pro automatizaci testů, jako jsou například testovací datové soubory aplikace Excel. Zadejte nebo vyberte například **C:\\Temp\\RegressionTool**.

        > [!NOTE]
        > Obsahuje-li název složky mezery, spuštění se nezdaří, protože složku nelze najít. Jedná se o známý problém, který by měl být opraven v nejnovější verzi nástroje.

    - **Výchozí prohlížeč** – Vyberte **Internet Explorer** nebo **Google Chrome**. Zkontrolujte, zda byly nainstalovány příslušné ovladače prohlížeče.
    - **Časový limit testovacího běhu** – určuje časový limit (v minutách) pro testovací běh. Po uplynutí časového limitu budou všechna aktivní okna zavřena a nevyřízené testovací případy selžou.
    - **Časový limit akce testu** – toto pole určuje časový limit (v minutách) pro požadavky serveru prostředí Finance and Operation. Obvykle by měla být dostatečná výchozí hodnota (2 minuty). V případě pomalejšího prostředí však může být vhodné hodnotu zvýšit, pokud dojde k chybám, které souvisejí s časovým limitem.
    - **Název společnosti** – zadejte název společnosti, který má být použit jako výchozí společnost při vytváření souborů parametrů aplikace Excel. Společnost lze později změnit úpravou souboru parametrů aplikace Excel.

    ![Dialogové okno Nastavení](./media/setup_rsa_tool_62.png)

4. Vyberte **Použít** k použití a uložení nastavení.

    Chcete-li uložit aktuální nastavení do konfiguračního souboru v počítači, vyberte možnost **Uložit jako**. Chcete-li obnovit nastavení z konfiguračního souboru v počítači, vyberte možnost **Otevřít**.

5. Zvolte **Zavřít** a zavřete dialogové okno.

### <a name="load-and-run-test-cases"></a>Nahrání a spuštění testovacích případů

1. Výběrem **Load** načtete **testovací plán RSAT** z projektu Azure DevOps.

    ![Tlačítko Odeslat](./media/setup_rsa_tool_64.png)

2. Vyberte testovací případ **Vytvořit nový produkt** z testovací sady a poté vyberte **Nový \> Generovat spuštění testu a soubory parametrů**.

    ![Příkaz Generovat spuštění testu a soubory parametrů v nabídce Nový](./media/setup_rsa_tool_65.png)

    Soubor parametrů **aplikace Excel je vytvořen v místní složce, kterou jste zadali v konfiguraci RSAT (například C:\\Temp\\RegressionTool**).

    ![Byl vytvořen soubor parametrů aplikace Excel.](./media/setup_rsa_tool_66.png)

3. Chcete-li uložit soubory parametrů, vyberte možnost **Odeslat**. Soubory automatizace všech vybraných testovacích případů jsou odeslány do Azure DevOps aplikace pro budoucí použití. (Tyto soubory zahrnují testovací soubory parametrů aplikace Excel.)

    Tímto způsobem můžete vybrat **Odeslat** pro načtení souborů parametrů (a automatizačních souborů) přímo z testovacího případu Azure DevOps. Soubory parametrů není nutné znovu vygenerovat. Tento přístup bude důležitý později, když chcete zachovat změny v souboru parametrů a nechcete, aby byly přepsány.

4. Chcete-li ověřit, zda jsou soubory automatizace a soubory parametrů uloženy do Azure DevOps, přejděte na projekt Azure DevOps, vyberte **Vývěsky \> Položky práce** a pak vyberte testovací případ **Vytvořit nový produkt**. Na kartě **přílohy** se zobrazí čtyři soubory:

    - **.cs** – C\# soubor automatizace
    - **. dll** – kompilovaný soubor automatizace jako sestava
    - **.xlsx** – soubor parametrů Excel
    - **.xml** – soubor záznamů

    ![Soubory na kartě Přílohy](./media/setup_rsa_tool_67.png)

5. Vyberte testovací případ, který se má spustit, a pak vyberte **Spustit**.

    > [!NOTE]
    > Před spuštěním testovacích případů v případě, že používáte prohlížeč Internet Explorer, zkontrolujte, zda je rozlišení plochy nastaveno na **100%** v **nastavení zobrazení systému Windows \> Měřítko a rozvržení**. Pokud toto nastavení nelze změnit u virtuálního počítače (VM), změňte jej na straně klienta (laptop), ze kterého se pokoušíte získat přístup k virtuálnímu počítači. Nastavení rozlišení pak zdědí nastavení zobrazení virtuálního počítače.

    ![Rozlišení plochy je nastaveno na 100 %](./media/setup_rsa_tool_68.png)

6. Nejsou-li ovladače prohlížeče v systému nainstalovány, zobrazí se varovná zpráva s upozorněním, že tato operace vyžaduje ovladač \<browser name\>. Chcete ho nyní automaticky stáhnout a nainstalovat? Vyberte **Ano**.

    ![Zpráva s upozorněním z aplikace Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Zpráva s upozorněním z aplikace Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > Pokud používáte prohlížeč Chrome a dostanete chybovou zprávu, že relace nebyla vytvořena, protože verze prohlížeče Chrome není správná, stáhněte si nejnovější ovladač Chrome ze stránek <http://chromedriver.chromium.org/downloads> do složky **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.

    ![Chybová zpráva aplikace Chrome](./media/setup_rsa_tool_71.png)

    Testovací případ je spuštěn a pole **Výsledek** je aktualizováno.

    ![Indikátor pokroku](./media/setup_rsa_tool_72.png)

    Pokud jste postupovali v tomto kurzu tak, jak je zapsán, testovací případ **Vytvořit nový produkt** se nezdaří, protože záznam úloh pro vytvoření produktu uložil název produktu jako pevně zakódovanou hodnotu. Pokud znovu spustíte stejný testovací případ, měli byste obdržet chybovou zprávu, protože produkt již existuje.

    ![Pole výsledku je nastaveno na nezdařilo se.](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>Zobrazení výsledků testu

1. Poklepejte na neúspěšný testovací případ.

    Dostanete chybovou zprávu.

    ![Chybová zpráva](./media/setup_rsa_tool_73.png)

2. Vyberte **Detaily** k zobrazení celé chybové zprávy.

    ![Celá chybová zpráva](./media/setup_rsa_tool_74.png)

3. Chcete-li zobrazit podrobnou verzi chybové zprávy v Azure DevOps, vyberte **Otevřít v Azure DevOps**. V Azure DevOps můžete zobrazit stav testovacího případu a podrobnou chybovou zprávu.

    ![Podrobná chybová zpráva v Azure DevOps](./media/setup_rsa_tool_75.png)

4. Chcete-li zobrazit výsledky testu přímo v projektu Azure DevOps, přejděte na **Test Plans \> Test Plans \> Runs**. Dvakrát klikněte na testovací běh, pro který chcete zobrazit podrobné informace.

    ![Seznam testovacích běhů v Azure DevOps](./media/setup_rsa_tool_76.png)

5. Na **Souhrn spuštění** je uvedeno, že testovací případ selhal, ale neposkytuje skutečnou chybovou zprávu. Chcete-li zobrazit podrobnou chybovou zprávu, vyberte kartu **Výsledky testu**.

    ![Karta Spustit souhrn](./media/setup_rsa_tool_77.png)

    Na kartě **Výsledky testu** jsou uvedeny informace o testovacím případu spolu s výstupem a chybovou zprávou.

    ![Karta Výsledky testu](./media/setup_rsa_tool_78.png)

6. Poklepáním na příslušný záznam zobrazíte podrobnou chybovou zprávu.

    ![Podrobná chybová zpráva](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > Všechny chybové zprávy jsou k dispozici také místně ve složce **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.

7. Výsledky testovacího běhu můžete exportovat také z úrovně plánu testování výběrem možnosti **Export**.

    ![Export testovacího plánu](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>Úprava souboru parametrů aplikace Excel

1. Otevřete RSAT.
2. Vyberte testovací případ a poté výběrem možnosti **Upravit** otevřete soubor parametrů aplikace Excel.

    Na listu **EcoResProductCreate** si povšimněte, že hodnota pole **Číslo produktu** je pevně kódována. Chcete-li znovu spustit testovací případ, je nutné toto pole aktualizovat na nové číslo produktu.

3. Chcete-li pro každý běh generovat jedinečné číslo produktu bez nutnosti znovu otevřít soubor parametrů aplikace Excel a ručně aktualizovat číslo produktu, použijte následující vzorec aplikace Excel.

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > Kromě karty **obecné** obsahuje soubor parametrů aplikace Excel kartu data pro každou stránku formuláře pro návštěvy testovacího případu.

    ![Pole Číslo produktu](./media/setup_rsa_tool_81.png)

4. Zvolte **Uložit** a pak zavřete sešit aplikace Excel.
5. Výběrem možnosti **Nahrát** uložte soubor parametrů aplikace Excel do Azure DevOps.

    ![Zpráva o úspěšném odeslání](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > Pokud chcete spustit testovací případy v určitém kontextu uživatele, zadejte do pole **Zkušební uživatel** na kartě **Obecné** souboru parametrů Excel ID e-mailu uživatele. V nejnovější verzi aplikace RSAT bylo aktualizováno rozložení polí v souboru parametrů aplikace Excel, ale koncept zůstává stejný.
    >
    > ![Pole Testovací uživatel](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>Ověření výsledků

- Výběrem **Spustit** znovu spusťte testovací případ a ověřte, zda byl testovací případ úspěšný. Výsledky testů můžete zobrazit způsobem popsaným v části [Zobrazení výsledků testu](#view-the-test-results).

    ![Pole výsledku je nastaveno na Úspěch](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>Zřetězení testovacích případů

Jedním klíčovým prvkem nástroje RSAT je zřetězení testovacích případů (tj. schopnost testu předat hodnoty jiným testům). Testovací případy se spouštějí podle jejich definovaného pořadí v testovacím plánu Azure DevOps. (Tuto objednávku lze také aktualizovat samotným testovacím nástrojem.) Chcete-li tedy předávat proměnné z jednoho testovacího případu do jiného, je velmi důležité, aby testy byly ve správném pořadí.

V tomto oddílu vytvoříte uloženou proměnnou v prvním testovacím případu, vytvoříte druhý testovací případ a předáte uloženou proměnnou z prvního testovacího případu do druhého testovacího případu. Testovací případy pak spustíte jako zřetězený testovací případ na kartě RSAT.

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>Úprava existujícího záznamu úlohy za účelem vytvoření uložené proměnné

1. Spusťte klienta.
2. Vyberte tlačítko **Nastavení** (symbol ozubeného kola) a poté vyberte položku **Záznamník úloh**.
3. Vyberte **Upravti záznam**.

    ![Tlačítko Upravit záznam](./media/setup_rsa_tool_85.png)

4. Vyberte **Otevřít ze služeb Lifecycle Services**

    ![Tlačítko Otevřít ze služeb Lifecycle Services](./media/setup_rsa_tool_86.png)

5. Vyberte **Vybrat knihovnu služeb Lifecycle Services**.

    ![Tlačítko Vybrat knihovnu služeb Lifecycle Services](./media/setup_rsa_tool_87.png)

    Knihovny BPM jsou načítány z LCS.

    ![Indikátor pokroku](./media/setup_rsa_tool_88.png)

6. Po načtení knihoven BPM z LCS vyberte knihovnu BPM **RSAT** a obchodní proces **Vytvořit nový produkt**, ke kterému byl záznam úkolu přidružen. Pak vyberte **OK**.

    ![Výběr knihovny BPM a obchodního procesu](./media/setup_rsa_tool_89.png)

7. Název příslušného záznamu úkolu je zadán do pole název **název záznamu**. Vyberte **Spustit**.

    ![Název záznamu úlohy v poli Název úlohy](./media/setup_rsa_tool_90.png)

8. Přejděte na **Správa informací o produktu \> Produkty** a vyberte **Nový** k otevření stránky, kde byla pořízena původní nahrávka úlohy **Vytvořit produkt**.
9. Vyberte **Vložit krok**.

    > [!NOTE]
    > Nový krok je vložen **za** krok, který jste vybrali v podokně.

    ![Tlačítko Vložit krok](./media/setup_rsa_tool_91.png)

10. Klepněte pravým tlačítkem myši na pole **Číslo produktu** a vyberte **Záznamník úloh \> Kopírovat**.

    ![Příkaz Kopírovat](./media/setup_rsa_tool_92.png)

11. V podokně je přidán nový krok. Poznamenejte si hodnotu v poli **Číslo produktu**, protože ji budete potřebovat později.

    ![Přidán nový krok](./media/setup_rsa_tool_93.png)

12. Vyberte **Dokončeny úpravy**.
13. Vyberte **Uložit do Lifecycle Services** a přiřaďte nový záznam úkolu ke stejné knihovně BPM a obchodnímu procesu, k němuž byl záznam původního úkolu přidružen. Další informace naleznete v tématu [Vytvoření záznamu úlohy a jeho uložení do oddílu knihovny BPM](#create-a-task-recording-and-save-it-to-the-bpm-library).
14. Přejděte do knihovny BPM a vyberte **Synchronizovat testovací případy** pro přepis záznamu úloh připojenému k testovacímu případu v Azure DevOps, jak je popsáno v části [Testování synchronizace z BPM do Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).
15. Otevřete RSAT a vyberte **Načíst**, chcete-li znovu načíst všechny testovací případy v sadě testů. Je nutné znovu vygenerovat soubory automatizace a parametrů pro příslušný testovací případ výběrem testovacího případu a následným výběrem **Nový \> Generovat soubory spuštění testu a parametry**, jak je popsáno v části [Načtení a spuštění testovacích případů](#load-and-run-test-cases).

    > [!NOTE]
    > Pokud byl soubor parametrů aplikace Excel ponechán otevřený, obnovení se nezdaří. Proto se ujistěte, že soubor parametrů aplikace Excel pro testovací případ je uzavřen před tím, než vygenerujete nový soubor parametrů aplikace Excel.

16. Vyberte **Upravit** k otevření nového souboru parametrů aplikace Excel. Bude zobrazena nová **uložená proměnná** položka na řádku 9. Tato proměnná **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, je uložena v souboru XML záznamu úkolu a lze ji použít v následných testech.

    ![Záznam uložené proměnné](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>Vytvoření nového testovacího případu

1. Přejděte do knihovny **RSAT** BPM.
2. Vyberte **příklad obchodního procesu podpory** a poté na pravé straně vyberte **režim úprav**.
3. Změňte hodnotu v poli **Název** a v poli **Popis** na **Vydat produkt**. Pak vyberte **Uložit**.

    ![Název a popis se změnil na Uvolnění produktu.](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>Vytvoření nového záznamu úlohy s funkcí ověření

- Vytvořte záznam úloh pro uvolnění produktu, který byl vytvořen dříve, do právnické osoby USRT. Další informace naleznete v tématu [Vytvoření záznamu úlohy a jeho uložení do oddílu knihovny BPM](#create-a-task-recording-and-save-it-to-the-bpm-library).

    > [!NOTE]
    > U zřetězených testovacích případů doporučujeme, abyste vyhledali nebo vyfiltroval záznam, který požadujete, *ručním zadáním hodnoty pole*. Tímto způsobem může nástroj určit záznam, proti němuž je akce provedena v následném testovacím případu.

    ![Nový záznam úlohy s funkcí ověření](./media/setup_rsa_tool_96.png)

    Jak ukazuje předchozí ilustrace, po nalezení produktu pomocí rychlého filtru, ale před tím, než vyberete **uvolněné produkty**, ověřte hodnotu pole **číslo produktu**, abyste se ujistili, že ID produktu je ID produktu, které bylo vytvořeno dříve. Chcete-li hodnotu ověřit, klepněte pravým tlačítkem myši na pole **Číslo produktu** a vyberte **Záznamník úloh \> Ověřit \> Aktuální hodnota**.

    ![Ověření aktuální hodnoty](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>Uložení záznamu úlohy do BPM

1. Po dokončení záznamu vyberte možnost **Uložit do Lifecycle Services**.

    ![Možnosti uložení](./media/setup_rsa_tool_98.png)

2. Informace o knihovně jsou načítány z LCS.

    ![Indikátor pokroku](./media/setup_rsa_tool_99.png)

3. Vyberte knihovnu BPM pro přidružení k záznamu úlohy. V tomto kurzu vyberte knihovnu **RSAT** BPM, která byla vytvořena dříve, a vytvořte v ní obchodní proces **Uvolnit produkt**. Pak vyberte **OK**.

#### <a name="sync-bpm-to-azure-devops"></a>Synchronizace BPM v Azure DevOps

1. Přejděte do knihovny BPM a otevřete knihovnu **RSAT**.
2. Vyberte **Synchronizace VSTS** a **Synchronizovat testovací případy**. Další informace naleznete v tématu [Testování synchronizace z BPM do Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).

    Po dokončení synchronizace se nová položka práce a odpovídající testovací případ pro obchodní proces **Uvolnit produkt** objeví v Azure DevOps v části **Vývěsky \> Položky práce**.

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>Přidání novéno testovacího případu do existující sady testů

1. Přejděte na **Testovací plány \> Testovací plány** a vyberte plán **RSAT Test Plan**.
2. Vyberte **Přidat existující**.
3. Na stránce **Přidat testovací případy do sady** vyberte možnost **spustit dotaz**.
4. Vyberte nový testovací případ, který byl vytvořen pro **uvolnění produktu** a poté vyberte možnost **přidat testovací případy** v pravém dolním rohu stránky (toto tlačítko není zobrazeno na následujícím obrázku).

    ![Stránka Přidat testovací případy do sady](./media/setup_rsa_tool_100.png)

    Sada testů nyní obsahuje dva testovací případy.

    ![Dva testovací případy v sadě testů](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>Nahrání testovacích případů do RSAT

1. Otevřete okno RSAT a vyberte **Načíst**.
2. Dojde k načtení testovacích případů a obdržíte upozornění, že tato akce přepíše soubory testovacích dat aplikace Excel, místní změny budou ztraceny. Chcete pokračovat? Výběrem **Ano** aktualizujete soubory parametrů aplikace Excel v místním systému, ale nepoužijete soubory parametrů aplikace Excel v Azure DevOps.

    ![Zpráva s upozorněním](./media/setup_rsa_tool_102.png)

    Oba testovací případy se načítají spolu se souborem parametrů aplikace Excel pro první testovací případ. Protože jste vybrali **Odeslat** při posledním spuštění, budou soubory parametrů načteny z Azure DevOps.

    ![Testovací případy odeslány](./media/setup_rsa_tool_103.png)

3. Vyberte pouze druhý testovací případ a poté vyberte **Nový \> Generovat soubory parametrů spuštění testu a parametrů**.

#### <a name="edit-the-excel-parameter-file"></a>Úprava souboru parametrů aplikace Excel

1. Vyberte jenom druhý testovací případ a poté výběrem možnosti **Upravit** otevřete odpovídající soubor parametrů aplikace Excel.
2. Zkopírujte uloženou proměnnou **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (viz [Modifikace existujícího záznamu úlohy k vytvoření uložené proměnné](#modify-an-existing-task-recording-to-create-a-saved-variable)) z prvního testovacího případu do všech polí, kde se používá číslo produktu. V takovém případě zkopírujte proměnnou do polí **Číslo produktu** a **Ověřit číslo produktu** v listu **EcoResProductListPage**.

    ![Pole Číslo produktu a Ověřit číslo produktu](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > Proměnné lze mezi testy přenášet pouze během jednoho testovacího běhu. Názvy proměnných se musí přesně shodovat.

3. Zvolte **Uložit** a pak zavřete sešit aplikace Excel.
4. Vyberte **Nahrát** pro uložení provedených změn do souboru parametrů aplikace Excel.

#### <a name="run-the-chained-test-cases"></a>Spuštění zřetězených testovacích případů

1. Vyberte oba testovací případy a pak vyberte **Spustit**.
2. Ověřte, zda oba testovací případy byly úspěšné.

    ![Pole výsledku nastavené na úspěch pro testovací případy](./media/setup_rsa_tool_105.png)
