node {
    script{
        def lastSuccessfulBuildID = 0
        def build = currentBuild.previousBuild
        while (build != null) {
            if (build.result == "SUCCESS")
            {
                lastSuccessfulBuildID = build.id as Integer
                break
            }
            build = build.previousBuild
        }
        println lastSuccessfulBuildID
    }
}
