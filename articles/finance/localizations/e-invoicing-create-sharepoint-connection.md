---
title: Konfigurace připojení SharePoint
description: Tento článek vysvětluje, jak nakonfigurovat připojení, aby elektronická fakturace měla přístup k webu SharePoint.
author: dkalyuzh
ms.date: 12/15/2021
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
ms.openlocfilehash: fb4258190b9480c1302060dd7b75145f80bb7f18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856573"
---
# <a name="configure-a-sharepoint-connection"></a>Konfigurace připojení SharePoint

[!include [banner](../includes/banner.md)]

Služba Elektronická fakturace umí číst soubory ze složek Microsoft SharePoint a nahrát soubory do služby SharePoint. Aby bylo zajištěno, že Elektronická fakturace bude mít přístup ke konkrétnímu webu SharePoint, musíte službě elektronické fakturace poskytnout přihlašovací údaje k webu. Abyste zajistili bezpečné uložení přihlašovacích údajů, neposkytujte je přímo. Místo toho je uložte do trezoru klíčů Azure a poskytněte tajný kód Azure Key Vault.

## <a name="grant-access-to-a-sharepoint-folder"></a>Udělení přístupu ke složce SharePoint

1. Vytvořte registraci aplikace v klientu, kde je nainstalována služba Regulatory Configuration Service (RCS).

    1. Přihlaste se do [portálu Azure](https://portal.azure.com/).
    2. Přejděte na **Registrace aplikací**.
    3. Vyberte **Nová registrace**.
    4. Zadejte název, například **Aplikace SharePoint pro elektronickou fakturaci** a dokončete registraci
    5. Vyberte registraci nové aplikace.
    6. Na kartě **Autentizace** zapněte možnost **Povolit veřejné klientské toky**.
    4. Na kartě **Certifikáty a tajné kódy** vyberte možnost **Nový tajný kód klienta** a vytvořte tajný kód klienta.
    5. Zkopírujte vytvořenou hodnotu tajného kódu.

    Postupujte podle následujících pokynů:

    - Nepoužívejte stejnou registraci aplikace pro různé služby.
    - Postupujte podle [doporučení zásad hesel](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - Nastavte rotaci hesel. Během rotace vytvořte nový tajný kód klienta pro registraci aplikace, aktualizujte trezor klíčů a poté odstraňte starý tajný kód.

2. Uložte hodnoty **Tajný kód registrace aplikace** a **ID aplikace (klienta)** jako dva nové tajné kódy v trezoru klíčů v nastavení vašeho prostředí elektronické fakturace.
3. Přidejte vytvořené tajné kódy do parametrů trezoru klíčů v nastavení prostředí Elektronické fakturace v RCS.
4. V portálu Azure udělte přístup do služby SharePoint. Tento krok by měl provést správce klienta.

    1. Vyberte vytvořenou registraci aplikace.
    2. Na kartě **Oprávnění API** vyberte **Přidat oprávnění**.
    3. Vyberte **Microsoft Graph (oprávnění aplikace)** \> **Sites.Selected**.
    4. Vyberte **Udělit souhlas správce pro \<user&nbsp;name\>**.
    5. Zkontrolujte pole **Stav**, abyste se ujistili, že oprávnění jsou udělena.

        ![Oprávnění udělená na kartě Oprávnění API.](media/configured-permissions.jpg)

    6. Otevřete nástroj [Průzkumník grafů - Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer) a přihlaste se.
    7. V levém podokně na kartě **Ukázkové dotazy** v části **Weby SharePoint** vyberte **získat web SharePoint na základě relativní cesty webu**.
    8. Vyplňte parametry **\{host-name\}** a **\{server-relative-path\}**. Například zapište `<domain>.sharepoint.com` jako parametr **\{host-name\}** a `sites/<siteName>` jako parametr **\{server-relative-path\}**.

        > [!NOTE]
        > U výchozího webu ponechte parametr **\{server-relative-path\}** prázdný.

    9. Vyberte příkaz **Spustit dotaz** a výsledek uložte.
    10. Nakonfigurujte následující dotaz.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        V tomto dotazu je **\{site-id\}** hodnotou uzlu **id** z předchozí odpovědi na dotaz.

        Zde je tělo žádosti.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        V tomto těle žádosti je **\{app-id\}** hodnotou **ID aplikace (klienta)** a **\{app-name\}** je **Název aplikace**.

        ![Dotaz POST.](media/app-id-query.jpg)

    11. Na kartě **Upravit oprávnění** vyberte **Otevřít panel oprávnění** a poté vyberte **Weby** \> **Sites.FullControl.All** \> **Souhlas**.
    12. Vyberte **Spustit dotaz**.

Služba Elektronická fakturace má nyní přístup k vašemu webu SharePoint.
