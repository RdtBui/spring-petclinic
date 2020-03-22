node {
    script{
        def lastSuccessfulBuildID = 0
        def lastSuccessfulHash = null
        def build = currentBuild.previousBuild
        
        while (build != null) {
            if (build.result == "SUCCESS")
            {
                lastSuccessfulBuildID = build.id as Integer
                lastSuccessfulHash = commitHashForBuild( lastSuccessfulBuildID )
                break
            }
            build = build.previousBuild
        }
        println lastSuccessfulHash
    }
}
def commitHashForBuild(build) {
  def scmAction = build?.actions.find { action -> action instanceof jenkins.scm.api.SCMRevisionAction }
  return scmAction?.revision?.hash
}
