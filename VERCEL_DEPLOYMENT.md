# Déploiement sur Vercel

## Variables d'Environnement Requises

Ajoutez ces variables dans les settings Vercel de votre projet :

```bash
# Supabase (récupérez depuis votre dashboard Supabase)
PUBLIC_SUPABASE_URL=https://[votre-projet].supabase.co
PUBLIC_SUPABASE_ANON_KEY=[votre-anon-key]
PRIVATE_SUPABASE_SERVICE_ROLE=[votre-service-role-key]

# Stripe (récupérez depuis votre dashboard Stripe)
PRIVATE_STRIPE_API_KEY=[votre-stripe-secret-key]
```

⚠️ **Important** : Les vraies clés sont dans votre fichier `.env.local` local. Ne les commitez jamais sur GitHub !

## Configuration Supabase

Après le déploiement, mettez à jour dans Supabase Dashboard :

1. **Authentication → URL Configuration**
   - Site URL : `https://votre-app.vercel.app`
   - Redirect URLs :
     - `https://votre-app.vercel.app/auth/callback`
     - `https://votre-app.vercel.app/auth/callback?*`

## Étapes de Déploiement

1. Allez sur [vercel.com](https://vercel.com)
2. Importez le projet depuis GitHub : `Damoc1ess/the_last_one`
3. Configurez les variables d'environnement ci-dessus
4. Déployez !

## Test des Paiements

Utilisez la carte test Stripe : `4242 4242 4242 4242`