---
title: Konfigurace prostředí nápovědy pro finanční a provozní aplikace
description: Tento článek poskytuje informace o součástech systému nápovědy pro některé aplikace Microsoft Dynamics 365.
author: edupont04
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: edupont
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.form: SystemParameters
ms.openlocfilehash: 75f3cc1b76b2a38d4004c4fa3f86a528a7eebc3f
ms.sourcegitcommit: d3f7a56eaf788d223ece4cedac4a319eaf5f6112
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/19/2022
ms.locfileid: "9538516"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>Konfigurace prostředí nápovědy pro finanční a provozní aplikace

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

V tomto článku najdete přehled součástí systému nápovědy pro finanční a provozní aplikace, jako je Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce a Dynamics 365 Human Resources. Tento článek také vysvětluje, jak tyto komponenty propojit, a poskytuje shrnutí procesu vytváření vlastní nápovědy.

## <a name="help-architecture"></a>Architektura nápovědy

Finanční a provozní aplikace zahrnují koncepční přehledy a další témata, která jsou publikována na webu [dokumentace Microsoft Dynamics 365](/dynamics365/). K tomuto obsahu lze poté přistupovat z podokna **Nápověda** v produktu. Následující obrázek znázorňuje části systému nápovědy.

[![Architektura nápovědy.](./media/help-architecture.png)](./media/help-architecture.png)

Systém nápovědy v produktu stahuje články z Microsoft Learn a dalších připojených webů. Načítá také průvodce záznamem úloh, které jsou uloženy v modelování podnikových procesů v Microsoft Dynamics Lifecycle Services (LCS).

## <a name="adding-task-guides"></a>Přidání průvodců záznamem úloh

> [!NOTE]
> Karta **Průvodci záznamem úloh** není k dispozici v aplikacích Human Resources či Commerce. <!--We are currently working to enable this functionality in a future release.--> Nicméně průvodci záznamem úloh v prostředí Začínáme v aplikaci Human Resources jsou i nadále k dispozici a zabývají se základními funkcemi. Procesní nápověda je k dispozici také na webu [dokumentace Microsoft Dynamics 365](/dynamics365/) pro Human Resources a Commerce.

Na stránce **Parametry systému** mohou správci systému nakonfigurovat přístup k příslušným knihovnám průvodců záznamem úloh pro implementaci.

> [!NOTE]
> - Chcete-li nakonfigurovat nápovědu, musíte se přihlásit pomocí účtu u stejného klienta jako je klient, ve kterém je aplikace umístěna.
> - Knihovnu LCS nelze připojit z instance aplikace spuštěné na místním virtuálním pevném disku (VHD).

[![Formulář Systémové parametry s nastavením nápovědy.](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Chcete-li nakonfigurovat průvodce záznamem úloh pro řešení, postupujte podle těchto kroků na stránce **Parametry systému**.

> [!IMPORTANT]
> Při prvním otevření karty **Nápověda** je nutné se připojit k službě Lifecycle Services. Zvolte odkaz uprostřed formuláře, počkejte na připojení, zavřete dialogové okno a volbou tlačítka **OK** otevřete stránku **Parametry systému**.
>
> [![Připojit k LCS](./media/connect-to-lcs-crop-1024x365.png "Připojení k LCS.")](./media/connect-to-lcs-crop.png)

1. Vyberte projekt služby Lifecycle Services pro připojení.
2. Vyberte knihovny BPM (v rámci vybraného projektu), ze kterých chcete načíst záznamy úkolů.
3. Nastavte pořadí zobrazení knihoven BPM. Toto pořadí zobrazení určuje pořadí, ve kterém se záznamy úkolů z knihoven zobrazí v podokně **Nápověda**.

Po dokončení těchto kroků můžete otevřít podokno **Nápověda** a vybrat kartu **Průvodci záznamem úloh**. Zobrazí se vám nyní průvodci záznamem úloh, které se vztahují ke stránce, na které se momentálně v finančních a provozních aplikacích nacházíte. Pokud nebyly nalezeny žádné průvodce úkolem, můžete zadat klíčová slova pro upřesnění hledání.

### <a name="showing-translated-task-guides"></a>Zobrazení přeložených průvodců úkoly

Přeložení průvodci záznamem úloh byli poprvé vydáni v knihovně APQC Unified Library pro květen 2016 a v knihovně Začínáme. Chcete-li zobrazit lokalizovanou nápovědu pro průvodce záznamem úloh, ujistěte se, že je vaše řešení Dynamics 365 připojeno ke knihovně z května 2016. Uživatelé mohou změnit jazyk, ve kterém se průvodce úkolem zobrazí, změnou jazykového nastavení v části **Možnosti** &gt; **Preference**.

> [!NOTE]
> I když mnoho průvodců záznamem úloh již bylo přeloženo, klient aktuálně nezobrazuje názvy přeložených průvodců záznamem úloh. Kromě toho jsou v knihovně z května 2016 k dispozici překlady pouze pro průvodce úloh, které byly vydány v únoru 2016. Aktualizovanou knihovnu s další překlady zpřístupní Microsoft později.
>
> - Pokud průvodce úkolem byl přeložen, veškerý text průvodce úkolem se při otevření daného průvodce zobrazí ve vybraném jazyce.
> - Pokud průvodce úkolem zatím nebyl přeložen, při otevření daného průvodce se zobrazí ve vybraném jazyce pouze některý text (text ovládacích prvků).

## <a name="adding-custom-help"></a>Přidání vlastní nápovědy

Můžete použít průvodce záznamem úloh k vytvoření vlastní nápovědy, nebo připojit vlastní webové stránky k podoknu **Nápověda**.

### <a name="create-custom-help-by-using-task-guides"></a>Vytvoření vlastní nápovědy pomocí průvodců záznamem úloh

Můžete si vytvořit vlastní nápovědu pro podporované aplikace vytvořením záznamů úloh, které odrážejí vaši implementaci, a poté je uložit do knihovny obchodních procesů v LCS. V aplikaci Human Resources nelze vytvářet vlastní průvodce záznamem úloh.

Pro partnery platí, že pokud knihovnu nastavíte jako podnikovou knihovnu a zahrnete ji do řešení, bude k dispozici vašim odběratelům. Můžete vytvořit také kopii sjednocené knihovny APQC a poté otevřít záznamy úloh v kopii, upravit je a uložit záznamy s provedenými změnami. Více informací viz [Zdroje záznamníku úloh](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-help-site"></a>Připojení vlastního webu nápovědy

Finanční a provozní aplikace se používají jen zřídka ve své výchozí formě. Místo toho je řešení přizpůsobeno a rozšířeno podle potřeb organizace. Můžete také přizpůsobit a rozšířit prostředí nápovědy. Například můžete přidat vlastní nápovědu do podokna **Nápověda** v produktu.

Společnost Microsoft poskytla sadu nástrojů, která vám pomůže při nasazení a připojení vlastní nápovědy k podoknu **Nápověda**. Informace o tom, jak můžete nastavit vlastní řešení nápovědy připojené k podoknu **Nápověda** najdete v části [Přehled vlastní nápovědy](../../dev-itpro/help/custom-help-overview.md).

Pokud chcete spolupracovat se společností Microsoft na nástrojích a procesech přizpůsobení nápovědy, vyplňte formulář na adrese [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).

## <a name="see-also"></a>Viz také

[Systém nápovědy](help-overview.md)  
[Přehled vlastní nápovědy](../../dev-itpro/help/custom-help-overview.md)  
[Zdroje záznamníku úloh](../../dev-itpro/user-interface/task-recorder.md)  
[Vytváření dokumentace nebo školení pomocí záznamníku úloh](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Úložiště GitHub vlastní nápovědy](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
