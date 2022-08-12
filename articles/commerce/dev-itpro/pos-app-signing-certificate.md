---
title: Podepsání MPOS souboru .appx pomocí certifikátu pro podepisování kódu
description: Tento článek vysvětluje, jak podepsat MPOS pomocí certifikátu pro podepisování kódu.
author: mugunthanm
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: 4cbdfcb5229be2f04531031c80f41f672b2a4747
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169092"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>Podepsání MPOS souboru .appx pomocí certifikátu pro podepisování kódu

[!include [banner](../includes/banner.md)]

Chcete-li nainstalovat Modern POS (MPOS), musíte aplikaci MPOS podepsat certifikátem pro podepisování kódu od důvěryhodného poskytovatele a nainstalovat stejný certifikát na všechny počítače, kde je nainstalován MPOS, a to do důvěryhodné kořenové složky pro aktuálního uživatele.

Chcete-li podepsat aplikaci MPOS pomocí certifikátu, použijte jednu z těchto možností v souboru **Retail SDK\\Build tool\\Customization.settings**:

- Přidejte část úkolu Zabezpečit soubor kroků sestavení Azure DevOps a nahrajte certifikát pro úlohu zabezpečení souboru. Použijte proměnnou výstupní cesty úlohy zabezpečení souboru jako parametr v souboru Customization.settings.

    > [!NOTE]
    > Úloha Zabezpečit soubor nepodporuje certifikát chráněný heslem. Před odesláním této úlohy musíte heslo odstranit. Protože se certifikát nahrává do úlohy zabezpečení souborového systému v Azure, můžete heslo odebrat pouze pro tento krok. Měli byste však odstranění hesla projednat se svými bezpečnostními experty, abyste zjistili, zda je to pro váš projekt správná akce. Neodstraňujte heslo certifikátu pro jiné scénáře.
- Použijte certifikát, který je v systému souborů. Chcete-li to provést, stáhněte nebo vygenerujte certifikát a umístěte jej do systému souborů tam, kde je spuštěno sestavení. Agent nebo uživatel sestavení hostovaný společností Microsoft by měl mít přístup k této cestě a souboru.
- Pomocí kryptografického otisku vyhledejte certifikát v úložišti a přihlaste se pomocí tohoto certifikátu.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Použití úkolu Zabezpečit soubor pro podepisování aplikací Univerzální platformy Windows

> [!NOTE]
> Azure Key Vault můžete také použít k uložení certifikátu a pomocí nástroje Azure Sign Tool podepsat soubor .appx aplikace Modern POS a samoobslužné instalační programy. Ukázkové skripty kanálu a další informace najdete v článku [Nastavení kanálu sestavení v Azure DevOps pro generování balíčků samoobslužného řešení pro maloobchod](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

Použití úlohy Zabezpečit soubor je doporučeným přístupem pro podepisování aplikací Univerzální platformy Windows. Další informace o podepisování balíčků najdete v článku [Konfigurace podepisování balíčků](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing). Tento proces vidíte na následujícím obrázku.

![Tok podepisování aplikace MPOS.](media/POSSigningFlow.png)

> [!NOTE]
> V současné době balíček OOB podporuje podepisování pouze u souborů .appx, různé samoobslužné instalační programy jako MPOIS, RSSU a HWS tímto procesem podepsány nejsou. Musíte je ručně podepsat pomocí nástroje SignTool nebo jiných nástrojů pro podepisování. Certifikát používaný k podepisování souborů .appx musí být nainstalován v počítači, kde je nainstalován Modern POS.

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Kroky konfigurace certifikátu pro podepisování v Azure Pipelines

### <a name="certificate-in-the-file-systemsecure-location"></a>Certifikát v systému souborů/zabezpečeném umístění

Stáhněte [úkol DownloadFile](/visualstudio/msbuild/downloadfile-task) certifikát a přidejte jej jako první krok v procesu sestavení. Výhodou použití úlohy Zabezpečit soubor je to, že soubor je zašifrován a umístěn na disk během sestavování bez ohledu na to, zda je sestavení úspěšné, selže nebo je zrušeno. Po dokončení procesu sestavení je soubor odstraněn z umístění pro stahování.

1. Stáhněte úkol Zabezpečit soubor a přidejte ho jako první krok v kanálu sestavení Azure. Úlohu Zabezpečit soubor si můžete stáhnout z [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).
1. Nahrajte certifikát do úlohy Zabezpečit soubor a v části Výstupní proměnné nastavte Referenční název, jak je znázorněno na následujícím obrázku.
    > [!div class="mx-imgBorder"]
    > ![Úkol Zabezpečit soubor.](media/SecureFile.png)
1. Vytvořte novou proměnnou v Azure Pipelines výběrem možnosti **Nová proměnná** na kartě **Proměnné**.
1. Zadejte název proměnné do pole hodnoty, např. **MySigningCert**.
1. Uložte proměnnou.
1. Otevřete soubor **Customization.settings** ve složce **RetailSDK\\BuildTools** a aktualizujte **ModernPOSPackageCertificateKeyFile** názvem proměnné vytvořené v kanálu (krok 3). Například:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    Tento krok je vyžadován, pokud certifikát není chráněn heslem. Pokud je certifikát chráněn heslem, pokračujte následujícími kroky.
    
1. Pokud chcete MPOS soubor .appx označit časovým razítkem při jeho podepisování certifikátem, otevřete soubor **Retail SDK\\Build tool\\Customization.settings** a do proměnné **ModernPOSPackageCertificateTimestamp** zapište poskytovatele časového razítka (například `http://timestamp.digicert.com`).
1. Na kartě **Proměnné** kanálu přidejte novou proměnnou zabezpečeného textu. Nastavte její název na **MySigningCert.secret** a nastavte hodnotu hesla pro certifikát. Chcete-li proměnnou zabezpečit, vyberte ikonu zámku.
1. Přidejte do kanálu úkol **Skript prostředí Powershell** (za krok Stáhnout zabezpečený soubor a před krok Sestavit). Zadejte **Zobrazovaný název** a nastavte Typ jako **Vložený**. Zkopírujte a vložte následující text do části skriptu.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. Otevřete soubor **Customization.settings** ve složce **RetailSDK\\BuildTools** a aktualizujte **ModernPOSPackageCertificateThumbprint** hodnotou kryptografického otisku certifikátu.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
Podrobnosti o tom, jak získat otisk pro certifikát, najdete v části o [načtení otisku certifikátu](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint). 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>Stáhněte si nebo vygenerujte certifikát pro ruční podepsání aplikace MPOS pomocí msbuild v SDK

Pokud je k podepsání aplikace MPOS použit stažený nebo vygenerovaný certifikát, aktualizujte uzel **ModernPOSPackageCertificateKeyFile** v souboru **BuildTools\\Customization.settings** tak, aby ukazoval na umístění souboru pfx (**$(SdkReferencesPath)\\appxsignkey.pfx**). Například:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

V tomto případě se souboru certifikátu jmenuje **appxsignkey.pfx** a nachází se ve složce **Retail SDK\\Reference**.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>Použití kryptografického otisku k podpisu aplikace MPOS

Pokud k podepisování aplikace MPOS používáte kryptografický otisk, nainstalujte certifikát lokálně. Aktualizujte hodnotu kryptografického otisku v uzlu **ModernPOSPackageCertificateThumbprint** souboru **BuildTools\\Customization.settings**.

Tato možnost bude fungovat, pokud je uživatel sestavení místním uživatelem. Pokud však k vygenerování sestavení používáte agenty Azure DevOps, pak agent nemusí mít oprávnění přístupu k úložišti certifikátů za účelem použití certifikátu k podepisování, nebo na počítači nebude certifikát nainstalován. V tomto případě je řešením změnit uživatele sestavení na místního uživatele a nainstalovat certifikát do počítače. Tato možnost však nebude fungovat, pokud k počítači nemáte přístup správce.

> [!NOTE]
> Pokud je k podepsání aplikace použit soubor .pfx nebo úloha Zabezpečit soubor, ponechte uzel **ModernPOSPackageCertificateThumbprint** v souboru **Customization.settings** prázdný. Pokud je použita možnost kryptografického otisku, ponechte uzel **ModernPOSPackageCertificateKeyFile** prázdný. Pokud jsou obě hodnoty aktualizovány, sestavení se nezdaří.

### <a name="certification-renewal"></a>Obnovení certifikátu

### <a name="renew-a-certificate-from-trusted-ca"></a>Obnovení certifikátu od důvěryhodné CA

S dotazy týkajícími se procesu obnovení certifikátu se obraťte na svou certifikační autoritu (CA). U důvěryhodného certifikátu není vyžadována na straně MPOS žádná akce.

### <a name="renew-a-self-signed-certificate"></a>Obnovení certifikátu podepsaného svým držitelem

V produkčním prostředí nepoužívejte vzorový certifikát dostupný v sadě Retail SDK. Slouží pouze pro vývojářské účely. Ukázkový certifikát Contoso nelze obnovit a platnost vzorového certifikátu obsaženého v Retail SDK verze 10.0.16 nebo starší vyprší 31. prosince 2020. Pokud byl tento certifikát nebo certifikát s vlastním podpisem použit k podpisu přizpůsobeného Modern POS, existuje velká pravděpodobnost, že Modern POS nebude po tomto datu správně fungovat.
 
### <a name="impact"></a>Dopad
 
Pokud pro vás platí výše uvedené sdělení, nebude možné spustit instalační program po 31. prosinci 2020. V závislosti na použitých firemních zásadách IT nemusí aplikace Modern POS fungovat. Je velmi důležité, abyste toto otestovali dočasnou změnou data na budoucí datum a určili dopad na vaši organizaci.
 
### <a name="steps-to-determine-the-issue"></a>Kroky k detekci problému
 
1.  V nastavení systému Windows změňte hodiny počítače na datum a čas v roce 2021.
2.  Ověřte, že lze otevřít aplikaci Modern POS, že je možné se do ní přihlásit a dokončit transakci.
3.  Ověřte, že lze spustit samoobslužný instalační program Modern POS, a pokud ano, že instalace bude úspěšně dokončena.
4.  Vraťte nastavení hodin systému Windows na správné datum a čas.
 
Pokud všechny tyto kroky provedete bez problémů, budete moci s aktuálním certifikátem pracovat po 31. prosinci 2020.  
 
### <a name="steps-going-forward"></a>Kroky do budoucna 

Důrazně doporučujeme obnovit dříve používaný certifikát. Důrazně doporučujeme získat nový certifikát. Chcete-li to udělat, musíte provést jednu z následujících akcí:
 
- **Upřednostňovaná** – Získejte certifikát pro podepisování kódu od důvěryhodné certifikační autority.

- **Neupřednostňovaná** – Vygenerujte certifikát pro podepisování kódu s vlastním podpisem, který chcete použít. Tato varianta se obvykle používá pouze pro vývojářské účely v rámci domény a nedoporučuje se pro produkční prostředí. 

- **K dispozici jako dočasné řešení** – Použijte obnovený certifikát pro podpis kódu Contoso. Tato varianta se obvykle používá pro testovací účely, takže se nedoporučuje, aby byla nasazena v produkci.
 
Dále vygenerujte nový přizpůsobený balíček Modern POS, který je podepsán pomocí certifikátu získaného jednou z výše uvedených akcí. V závislosti na certifikátu je třeba provést jeden z následujících kroků:
 
- Pokud používáte nový, důvěryhodný certifikát (nebo nový certifikát podepsaný svým držitelem), budete muset nainstalovat nový certifikát na každé zařízení. Poté musíte vzít nově vytvořený balíček Modern POS (instalátor), odinstalovat stávající aplikaci a poté znovu nainstalovat nový balíček Modern POS. Na každém zařízení budete muset provést aktivaci zařízení Modern POS.

- Pokud používáte obnovený certifikát Contoso, budete muset nainstalovat nový certifikát na každé zařízení a nainstalovat balíček Modern POS Package (instalátor). Není nutné odebírat instalaci, ale musíte ho znovu nainstalovat na zařízení. Upozorňujeme, že aktivace zařízení Modern POS nebude vyžadována. Tato možnost je dočasným řešením. Tuto možnost použijte pouze k zamezení opětovné aktivace a vyřešení problému před získáním nového důvěryhodného certifikátu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
