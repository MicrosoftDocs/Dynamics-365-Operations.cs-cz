---
title: Odstraňování problémů s nastavením a instalací služby Store Commerce
description: Tento článek vysvětluje, jak řešit problémy s nastavením a instalací v aplikaci Microsoft Dynamics 365 Commerce Store Commerce.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 92d4a9d78485b681b4e802f695d54f44ecd7c5de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870459"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Odstraňování problémů s nastavením a instalací služby Store Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tento článek vysvětluje, jak řešit problémy s nastavením a instalací v aplikaci Microsoft Dynamics 365 Commerce Store Commerce.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>Nemohu aplikaci aktivovat a zobrazuje se mi chybová zpráva o připojení

Po zadání platné adresy URL Cloud Point of Sale (CPOS) se může zobrazit chybová zpráva připojení podobná následujícímu příkladu:

> Došlo k chybě připojení a vaše zařízení se nemůže připojit k CPOS. Zadaná adresa URL CPOS může mít nějaké problémy.

V tomto případě zkontrolujte adresu URL, zda neobsahuje typografické chyby, nebo zjistěte, zda není CPOS nedosažitelné, protože je offline.

Dále ověřte, že verze Cloud Scale Unit (CSU) je 10.0.25 (9.35.\*.\*) nebo novější. K používání aplikace Store Commerce je vyžadována verze CPOS 10.0.25 nebo novější.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Nemohu nainstalovat aplikaci, protože Modern POS je již nainstalován

Při instalaci se může zobrazit chybová zpráva jako v následujícím příkladu:

> Verze (9.\*.\*.\*) tohoto produktu (moderní POS) byla dříve nainstalována prostřednictvím staršího instalačního programu.

Chcete-li chybu opravit, musíte odinstalovat aplikaci Modern Point of Sale (MPOS) pro všechny uživatele na počítači a potom to zkusit znovu. Zda byla aplikace MPOS odebrána pro všechny uživatele, můžete potvrdit spuštěním následujícího příkazu PowerShell.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Nemohu aplikaci aktivovat z důvodu neplatné adresy URL nebo chybového stavu

Pokud zadaná adresa URL CPOS není platná a chcete ji změnit nebo pokud je aplikace Store Commerce během aktivace v chybovém stavu, můžete proces restartovat resetováním aplikace. Aplikace Store Commerce uloží pouze platnou adresu URL CPOS.

Chcete-li resetovat aplikaci Store Commerce, postupujte takto.

1. V nabídce **Start** systému Windows vyberte a podržte (nebo klikněte pravým tlačítkem) na aplikaci a poté vyberte **Více \> Nastavení aplikace**.
2. Posouvejte dolů stránku nastavení aplikace, dokud nenajdete tlačítko **Resetovat**.
3. Vyberte **Obnovit**. Až budete vyzváni k potvrzení odebrání modulu, potvrďte, že chcete aplikaci resetovat.
